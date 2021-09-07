# Org-api

This is a spark-java api that enables one dispay the data from a database in form of a json object;

## Author

- **Edwin Kaburu**





## Getting Started

Clone this repository to your local machine to get Started

Github: [https://github.com/Misanthrope555/Organization-API](https://github.com/Misanthrope555/Organization-API.git)

### Prerequisites

You need the following installed on your machine

- java
- JDK - Java Development Kit
- Maven
- Gradle
- An IDE - Intellij
- Postman - for testing the api

To confirm run the following command on linux

```
$ java --version       //java version
$ mvn --version        //maven version
$ gradle --version     //gradle version
```

## Installing

After cloning to your local machine navigate to the folder you cloned into and open it with intellij.

- Navigate into the `src/main/java/App.java` and open it in intellij idea or your favorite editor.
- Go to your browser and type `localhost:4567`

After this you will probably get a 500 error since we do not have a database yet.
```
in psql:
CREATE DATABASE org_api_test;
CREATE TABLE IF NOT EXISTS news(id SERIAL PRIMARY KEY, news VARCHAR, departmentId int);
CREATE TABLE IF NOT EXISTS departments(id SERIAL PRIMARY KEY,departmentid int,departmentname VARCHAR);

//for the test database
In psql:
CREATE DATABASE wildlife_tracker_test WITH TEMPLATE wildlife_tracker;

```

## Running the App
Navigate to the project directory through your terminal and type gradle run.


Your code should look something like this where moringa is your computer username

```

moringa@moringa-Lenovo-V110-15ISK:~/moringa-projects/JAVA/wild$ gradle run

```


## Running the Tests

Create a test class for running tests in the application.

This is a sample test that tests if the method adding animals to the database works

```

@Test
public void update() {
    News news = setUpNews();
    String newsString = news.getNews();
    newsDao.update(newsDao.getAll().get(0).getId(),"New news",3);
    assertEquals("New news",newsDao.getAll().get(0).getNews());
}

```

## Built With

- [Java](https://www.java.com/) - The language used
- [Intellij Idea](https://www.jetbrains.com/idea/) - Intergated development
- [Spark]() - Framework

## Contributing

If you want to put out a pull request you first have to send us the sample code that you want to add to our repository for cross-checking before we allow the pull.

## Versioning

We use [Github](https://github.com/) for versioning. This is the first version of this application

## License

This project is licensed under the MIT License -see the [LICENSE](LICENSE) file for details

## Acknowledgments

- Hat tip to `Stackoverflow`
