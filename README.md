# 🧠 SmartDevAnalyzer

**SmartDevAnalyzer** est un outil intelligent développé avec **Java 17** et **Spring Boot**. Il permet aux développeurs backend de scanner automatiquement leurs projets Java afin de :

## 🔐 1. Détecter des failles de sécurité :
- Contrôleurs non protégés (ex: absence de `@PreAuthorize`, `@Secured`, ou filtre de sécurité)
- Informations sensibles codées en dur (ex: mots de passe, tokens)
- Dépendances vulnérables connues (analyse du `pom.xml` via **OWASP Dependency Check**)

## 📘 2. Générer une documentation automatique des APIs REST :
- Lecture des `@RestController`, `@RequestMapping`, `@GetMapping`, etc.
- Extraction automatique des chemins, méthodes HTTP, types de retour, et paramètres
- Génération en **JSON** ou **Markdown** d’un équivalent de Swagger (mais maison)

---







## 🧰 Stack technique

| Composant         | Technologie            |
|------------------|------------------------|
| Langage          | Java 17                |
| Framework        | Spring Boot            |
| Analyse Code     | JavaParser             |
| Analyse Sécurité | OWASP Dependency-Check |
| Logger           | SLF4J + Logback
|Tests	           | JUnit







---







## 🧱 Architecture du projet



![image](https://github.com/user-attachments/assets/d75bb36e-2618-4d6f-b67f-5c7b4b96e584)




---







## 🚀 Utilisation

Cloner le projet :

-git clone https://github.com/elkadirizouhra/smartdev-analyzer.git
-cd smartdev-analyzer
-Construire et lancer :

-mvn clean install
-mvn spring-boot:run -Dproject.path=/chemin/vers/le/projet

Sortie attendue :
Un fichier report.json contenant les endpoints et les problèmes de sécurité détectés
Un fichier apidoc.json ou apidoc.md avec la documentation générée

📄 Exemple de sortie
[
  {
    "method": "GET",
    "path": "/api/users",
    "controller": "UserController",
    "secured": false,
    "returns": "List<User>"
  }
]


---







## 🧪 À venir

Analyse statique plus poussée (ex: injection SQL)

Génération HTML de la documentation

Intégration CLI avec Docker

🤝 Contribution
Forkez, proposez vos améliorations, ouvrez une Pull Request.
Projet personnel de Zahira Elkadiri – 2025

