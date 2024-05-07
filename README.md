package com.company;

public class Main {

    public static void main(String[] args) {
	// write your code here
        Person person = new Person("Димон", "Нагиев", 1967);
        Car car = new Car("Mercedes-AMG S 63 Coupe", 2017, 4.0);
        Book book = new Book("'Ремонт и руководство по эксплуатации Mercedes-AMG S 63 Coupe'", "Mercedes-Benz", 2017);
        person.PersonDisplayInfo();
        car.CarDisplayInfo();
        book.BookDisplayInfo();
        person.Finaly(car,book);
    }
}
class Person{
    static String name;
    String surName;
    int birthYear;
    public Person(String name, String surName, int birthYear){
        this.name=name;
        this.surName=surName;
        this.birthYear=birthYear;
    }
    public void PersonDisplayInfo(){
        System.out.println("Человек:" + " " + name + " " + surName + ", дата рождения: " + birthYear);
    }
    public void Finaly( Car car, Book book){
        System.out.println(name+ " " + "читает книгу " + book.bookTitle  + " про машину " + car.brand);
    }

}
class Car {
    String brand;
    int year;
    double engineV;

    public Car(String brand, int year, double engineV) {
        this.brand = brand;
        this.year = year;
        this.engineV = engineV;
    }

    public void CarDisplayInfo() {
        System.out.println("Автомобиль: " + brand + " " + year + " года выпуска, объем двигателя - " + engineV);
    }
}

class Book {
    String bookTitle;
    String author;
    int releaseYear;

    public Book(String bookTitle, String author, int releaseYear) {
        this.bookTitle = bookTitle;
        this.author = author;
        this.releaseYear = releaseYear;
    }

    public void BookDisplayInfo() {
        System.out.println("Книга: " + bookTitle + ", автор: " + author + ", год выпуска: " + releaseYear);
    }
}
