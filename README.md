# Дипломный проект курса «Тестировщик ПО»

## Описание

Программа предназначена для покупки тура двумя способами: с помощью дебетовой картой или с помощью кредита.

## Документация проекта
* [Планирование автоматизации]()
* [Отчетный документ по итогам тестирования]()
* [Отчетный документ по итогам автоматизации]()

## Необходимое ПО
* Browser;
* Java11; 
* IntelliJ IDEA;
* Docker.

## Инструкция по запуску
1. Склонировать репозиторий по [ссылке]();
1. Открыть программу InteliJ Idea, вкладку Terminal и развернуть базу данных командой  `docker-compose up -d --force-recreate`
1. Запустить тестируемое приложение командой :
    * если используете СУБД Postgres: `java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/postgres -jar artifacts/aqa-shop.jar`
    * если используете СУБД MySQL: `java -Dspring.datasource.url=jdbc:mysql://localhost:3306/app -jar artifacts/aqa-shop.jar`
1. Запустить тесты командой:
    * при работе с Postgres: `gradlew clean test -Ddb.url=jdbc:postgresql://localhost:5432/postgres`
    * при работе с MySql: `gradlew clean test -Ddb.url=jdbc:mysql://localhost:3306/app`