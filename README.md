# Apache Spark + JDK: Полный гайд по установке (Windows & macOS)

Этот туториал показывает, как с нуля установить **Apache Spark** и **JDK** так, чтобы:

- Spark работал из терминала/командной строки;
- можно было проверять версии и запускать простые примеры;
- студенты могли повторить шаг за шагом.

## 0. Рекомендуемые версии

**Рекомендованный стек (и для Windows, и для macOS):**

| Компонент    | Версия                               |
|--------------|--------------------------------------|
| Java (JDK)   | **JDK 17 (LTS)**                     |
| Apache Spark | **Spark 3.5.7 (`spark-3.5.7-bin-hadoop3`)** |

Spark 3.5.x официально поддерживает Java 8/11/17, поэтому JDK 17 — безопасный выбор на несколько лет вперёд.

---

## Часть A. Установка Apache Spark 3.5.7 на Windows 10/11

### A1. Устанавливаем JDK 17 (Windows)

1. Скачайте JDK 17 (любую OpenJDK-сборку), например:
   - (https://download.oracle.com/java/17/archive/jdk-17.0.12_windows-x64_bin.exe)
   - или Microsoft OpenJDK 17
2. Установите JDK (Next–Next–Finish).
   Типовой путь:
   - `C:\Program Files\Eclipse Adoptium\jdk-17.x.x.x-hotspot`
   - или `C:\Program Files\Java\jdk-17.x.x`

3. Проверьте установку в **cmd**:

   ```cmd
   java -version

openjdk version "17.0.11" 2024-04-16
OpenJDK Runtime Environment ...
OpenJDK 64-Bit Server VM ...

### Устанавливаем Apache Spark 3.5.7
https://dlcdn.apache.org/spark/spark-3.5.7/spark-3.5.7-bin-hadoop3.tgz


### Если Spark не запускается или не создаётся SparkContext:

`java -version`
Убедитесь, что используется Java 17, а не 1.8 / 11 / 21.

`JAVA_HOME`

#### Windows: `echo %JAVA_HOME%`

#### macOS: `echo $JAVA_HOME`
#### Путь должен указывать на директорию JDK 17.

`SPARK_HOME`

#### Windows: `echo %SPARK_HOME%`

#### macOS: `echo $SPARK_HOME`
#### Должен указывать на директорию spark-3.5.7-bin-hadoop3.

`PATH`
#### В PATH должны фигурировать:

Windows: `%JAVA_HOME%\bin`, `%SPARK_HOME%\bin`, `%HADOOP_HOME%\bin` (если на Windows).

macOS: `$JAVA_HOME/bin`, `$SPARK_HOME/bin`.

 Проверка `spark-shell --version`
Если shell вообще не стартует — ошибка в `JAVA_HOME` или `SPARK_HOME`.

#### Для Windows:

 Проверьте наличие `C:\hadoop\bin\winutils.exe`.

 Проверьте переменную `HADOOP_HOME` и наличие `%HADOOP_HOME%\bin` в `Path`.

#### Для Jupyter:
Установлен ли пакет pyspark в той же среде, где запущен Jupyter (`pip show pyspark`)?

Не конфликтуют ли несколько версий Python / разные окружения?

