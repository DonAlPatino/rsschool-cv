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