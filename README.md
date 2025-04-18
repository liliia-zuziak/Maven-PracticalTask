# Practical Task Report: Spring Petclinic Maven Release

## 1. Install Java and Maven 
- **Commands used**:
```bash
brew install openjdk
brew install maven
```
- **Result**:  


![alt text](<Screenshot 2025-04-16 at 16.40.09.png>)
![alt text](<Screenshot 2025-04-16 at 16.41.08.png>)
---

## 2. Clone Spring Petclinic Repository
- **Command used**:
```bash
git clone https://github.com/liliia-zuziak/spring-petclinic
cd spring-petclinic
```
- **Result**:  


![alt text](<Screenshot 2025-04-16 at 16.44.56.png>)
---

## 3. Validate Project with Maven
- **Command used**:
```bash
mvn validate
```
- **Result**:  

![alt text](<Screenshot 2025-04-16 at 16.48.41.png>)
![alt text](<Screenshot 2025-04-16 at 16.49.20.png>)
---

## 4. Package JAR and Run the Application
- **Commands used**:
```bash
mvn package
java -jar target/*.jar
```
- **Result**:  
Application built and launched successfully.

![alt text](<Screenshot 2025-04-16 at 16.53.21.png>)
![alt text](<Screenshot 2025-04-16 at 16.55.24.png>)
![alt text](<Screenshot 2025-04-16 at 16.56.43.png>)
![alt text](<Screenshot 2025-04-16 at 16.57.01.png>)

---

## 5. Update Project Version to 4.0.0
- **Manual update**:
```xml
<version>4.0.0-SNAPSHOT</version>
```
- **Result**:  
Version updated in `pom.xml`.

![alt text](<Screenshot 2025-04-16 at 17.13.56.png>)
---

## 6. Add SCM Section and Release Plugin


![alt text](<Screenshot 2025-04-16 at 17.13.49.png>)
---

## 7. Prepare Release
- **Command used**:
```bash
mvn release:clean release:prepare -Darguments="-DskipTests" -B
```
- **Result**:  
Release preparation completed successfully.

![alt text](<Screenshot 2025-04-16 at 17.20.27.png>)
![alt text](<Screenshot 2025-04-16 at 17.21.25.png>)
---

## 8. Perform the Release
- **Command used**:
```bash
mvn release:perform -Darguments="-DskipTests"
```
- **Result**:  
Artifacts released successfully. New version initialized.

![alt text](`.png)
![alt text](2.png)
---

## 9. Perform Release Cleanup
- **Command used**:
```bash
mvn release:clean
```
- **Result**:  
Cleanup after release completed successfully.

![alt text](3.png)