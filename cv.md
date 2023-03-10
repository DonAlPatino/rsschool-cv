# Viacheslav Alpatov

![photo](slava.png "А это я")

## My Contact Info

* **City:** *Moscow*
* **LinkedIn:** *[Viacheslav Alpatov](https://www.linkedin.com/in/viacheslav-alpatov/)*
* **GitHub:** *[DonAlPatino](https://github.com/DonAlPatino)*
* **Discord:** *Viacheslav(@DonAlPatino)*


## About me

I was IT Manager in small russian companies for long time. Now I want to become a software developer.

## Skills

* Windows, Linux, MacOS, VMware ...
* SQL, MS SQL, Postgres, Oracle
* Java/Spring (junior)
* Python (junior)
* HTML/CSS/JavaScript (junior)
* ... and all that managment staff

--------------

## Code examples

```java
import org.hibernate.Session;
import org.springframework.stereotype.Component;
import org.springframework.transaction.annotation.Transactional;
import ru.alpatov.SpringShop.models.Book;

import javax.persistence.EntityManager;
import javax.persistence.PersistenceContext;
import java.util.List;


/**
 * @author Viacheslav Alpatov
 */
@Component
public class BookDao {

    @PersistenceContext
    private EntityManager entityManager;

    @Transactional(readOnly = true)
    public List<Book> findOrderedBooks(){
        Session session = entityManager.unwrap(Session.class);
        List<Book> books = session.createQuery("select b from Book b join fetch b.purchases p join fetch p.account").getResultList();
        return books;
    }
}
```
--------------
## Experience

20 years of IT management 

## Education

* **The Russian University for Humanities, Moscow**
    * Faculty of Information Technologies, graduate at information science
* **International Institute of Management LINK , Moscow**
    * Presidential Managers' Training Program- «Management in Business»

## Professional development, courses

Year|Course Name|Academy
----|-----------|-------
2023|Ansible - From Zero to Professional|Udemy
2022|"Websoft HСM Administrator. Advanced Level"|Globex IT
2022|Introduction to enterprise Java development|Innopolis University, java junior developer
2021|MS-030T00-A: Office 365 Administrator|Softline
2021|MS-101T00: Microsoft 365 Mobility and Security|Softline
2021|MS-500T00-A - Microsoft 365 Security Administration|Softline
2021|MS-700T00: Managing Microsoft Teams|Softline
2016|DevOps: What, Why, and How. An Introduction to DevOps|EMC Education Service
2016|«Web technology» (Python Django)|mail.ru/stepic.org
2015|Online school for android developers|E-legion &Google
2014|Professional work in 1C:Payroll and HR 8 ed.3|Profbuh, certificate
2013|IT Management with clouds|CIO Academy
2012|Data conversion in 1C|1C
2012|Integration and data exchange in 1C|1C
2011|«IT security»|Inforzashita