  # Дипломный проект профессии "Тестировщик"


- *Описание проекта* ->[Project Description]( https://github.com/netology-code/qa-diploma/tree/2ccafd34b6f9eb3a66dd7a11a0b8b1ba3f266e50#%D0%B4%D0%B8%D0%BF%D0%BB%D0%BE%D0%BC%D0%BD%D1%8B%D0%B9-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82-%D0%BF%D1%80%D0%BE%D1%84%D0%B5%D1%81%D1%81%D0%B8%D0%B8-%D1%82%D0%B5%D1%81%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D1%89%D0%B8%D0%BA)
______________________________________

- *Отчетная документация процесса работы над проектом* :

    * [План автоматизации тестирования](https://github.com/ValeriaBorisova/Diplom-JAVA/blob/master/Documentation/Plan.md)
    * [Отчёт о проведенном тестировании](https://github.com/ValeriaBorisova/Diplom-JAVA/blob/master/Documentation/Report.md)
    * [Отчёт о проведенной автоматизации тестирования](https://github.com/ValeriaBorisova/Diplom-JAVA/blob/master/Documentation/Summary.md)
__________________________________

- *Предварительная установка и подготовка необходимого окружения*:

    * IDE - [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows) - необходимо выбрать установочный файл согласно предустановленной ОС на локальной машине
    * JAVA 11.0.13 [установка](https://www.oracle.com/java/technologies/downloads/) - необходимо выбрать установочный файл согласно предустановленной ОС на локальной машине
    * Система контроля версий - [Git](https://git-scm.com/downloads) - необходимо выбрать установочный файл согласно предустановленной ОС на локальной машине
    * DOCKER:
    
         - Для ОС Windows и Linux:
         
            * Необходима предварительная установка [DockerToolbox и VirtualBox](https://it-black.ru/ustanovka-docker/) :
              
      ⚠️Особое внимание следует уделить обладателям машин с предустановленной OC Windows  + процессор AMD ⚠️ 
             
                Необходим дополнительный скрипт ```docker-machine create default --virtualbox-no-vtx-check```
    
            * Docker Desctop [устоновка](https://www.docker.com/products/docker-desktop)
            
         - Для ОС MacOS:
          
            *  Docker Desctop [устоновка](https://www.docker.com/products/docker-desktop)
     * DBeaver [установка](https://dbeaver.io/download/) -  необходимо выбрать установочный файл согласно предустановленной ОС на локальной машине
     * Стабильное интернет соединение - предпочтительно по Wi-Fi
_____________________________________

- ***Процедура запуска автотестов*** :

     * Клонировать репозиторий [git clone](https://github.com/ValeriaBorisova/Diplom-JAVA.git)
     * На локальной машине запустить ```IntelliJ IDEA``` с системой сборки ```Gradle``` и версией ```JAVA 11.0.13```
     * Открыть клонированный репозиторий : в ```Terminal IntelliJ IDEA```  выполнить скрипт [git clone](https://github.com/ValeriaBorisova/Diplom-JAVA.git)
     * В [Docker Desctop](https://www.docker.com/products/docker-desktop) выполнить скрипты ```docker pull mysql``` и ```docker pull postgres```
     * В ```Terminal IntelliJ IDEA```  выполнить скрипт ```docker run -d -p 80:80 docker/getting-started```
     * Запустить SUT :
          - Для ОС Windows и Linux : выбрать директорию ```artifacts``` -> ```Open in``` -> ```Terminal``` ->         
                                    выполнить скрипт ```java -jar artifacts/aqa-shop.jar```
          
          - Для ОС MacOS : ```Terminal``` ->  выполнить скрипт ```java -jar artifacts/aqa-shop.jar```
    * Для запуска автотестов в  ```Terminal IntelliJ IDEA```  выполнить скрипт ```./gradlew clean test allureReport -Dheadless=true```
    * Для просмотра отчета ```Allure-Report``` в ```Terminal``` выполнить скрипт ```./gradlew allureServe```
    
    * Запуск ***приложения*** под Базы Данных:
        - MySQL ```java -Dspring.datasource.url=jdbc:mysql://localhost:3306/app -jar aqa-shop.jar```
        - PostgreSQL ```java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/app -jar aqa-shop.jar```
        
    * Запуск автотестов под запущенные Базы Данных:
        - MySQL ```gradlew -Ddb.url=jdbc:mysql://localhost:3306/app clean test```
        - PostgreSQL ```gradlew -Ddb.url=jdbc:postgresql://localhost:5432/app clean test```
        
    * После окончания тестов завершить работу приложения ```Ctrl+C```, остановить контейнеры командой ```docker-compose down```
________________

- Конфигурация настройки CI находтся в предоставленном  [файле](https://github.com/ValeriaBorisova/Diplom-JAVA/blob/master/.appveyor.yml)

[![Build status](https://ci.appveyor.com/api/projects/status/gk3beaevlirjb5py?svg=true)](https://ci.appveyor.com/project/ValeriaBorisova/diplom-java)

       
