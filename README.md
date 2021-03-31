# Lab2: SQL injection UNION attack, finding a column containing text

Bu yazıda, PortSwingger tarafından oluşturulan SQLi lablarının ikincisini inceleyeceğiz. Bu labta bir sütunun dize verileriyle uyumlu olup olmadığını nasıl belirleyeceğimizi göreceğiz.

Lab yönergesi:


This lab contains an SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. To construct such an attack, you first need to determine the number of columns returned by the query. You can do this using a technique you learned in a previous lab. The next step is to identify a column that is compatible with string data.

The lab will provide a random value that you need to make appear within the query results. To solve the lab, perform an SQL injection UNION attack that returns an additional row containing the value provided. This technique helps you determine which columns are compatible with string data. 
(Laboratuarı çözmek için, sağlanan değeri içeren ek bir satır döndüren bir SQL injection UNION saldırısı yapacağız.)
![image](https://user-images.githubusercontent.com/70814577/112759128-4b214680-8ffa-11eb-8127-f8cf763ef189.png)

Bu laboratuvarda, ilk labdaki gibi UNION saldırı tekniğini kullanacağız ancak SELECT sütunu tarafından hangi veri türünün döndürüleceğini belirleyeceğiz bunun için veritabanının "bUuJw" dizesini döndürmesini sağlayacağız.

Hatanın yerini ve çözülecek problemi belirledikten sonra laboratuvara gidip ilk labta yaptığımız gibi  ‘+UNION+SELECT+NULL,NULL,NULL– ve sorgunun döndürdüğü sütun sayısı için bir arama yapıyoruz.
![image](https://user-images.githubusercontent.com/70814577/112753942-7e57db80-8fe2-11eb-9035-e9564115a75d.png)
![image](https://user-images.githubusercontent.com/70814577/112753975-aa735c80-8fe2-11eb-9127-7c8004af912a.png)
![image](https://user-images.githubusercontent.com/70814577/112753992-c70f9480-8fe2-11eb-89a1-59be26d58943.png)
![image](https://user-images.githubusercontent.com/70814577/112754004-d42c8380-8fe2-11eb-82b9-340d2b95db0c.png)

Sütün sayısını bulduktan sonra, sorgunun 1. sütununun sonucunu "bUuJw" dizesiyle birleştiriyoruz. Sorgunun 1. sütununun sonucu da bir dizeyse, sorgunun 1. sütunu 'bUuJw' dizesiyle döndürülür ve sorgunun 1. sütunu başka bir veri türündeyse (örneğin, INT, BOOLEAN, ...), sorgu başarısız olur. 
![image](https://user-images.githubusercontent.com/70814577/112754042-06d67c00-8fe3-11eb-9875-e761cc821003.png)

Sorgu başarısız oldu. Bu da sorgunun 1. sütununun dize türünde olmadığı anlamına gelmektedir. Aynı şeyi 2. sütun için de yapıyoruz:
![image](https://user-images.githubusercontent.com/70814577/112754074-279ed180-8fe3-11eb-8133-61b190d8323d.png)
Sorgunun hata vermediğini ve "bUuJw" dizesini döndürdüğünü gözlemleyebilirisiniz. Sonuç olarak sorgunun ikinci sütununun dize türünü döndürdüğünü biliyoruz.
