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
   - Adoptium Temurin 17 (MSI для Windows x64)
   - или Microsoft OpenJDK 17
2. Установите JDK (Next–Next–Finish).
   Типовой путь:
   - `C:\Program Files\Eclipse Adoptium\jdk-17.x.x.x-hotspot`
   - или `C:\Program Files\Java\jdk-17.x.x`

3. Проверьте установку в **cmd**:

   ```cmd
   java -version
