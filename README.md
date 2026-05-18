# Resume Builder

A desktop application for creating professional PDF resumes with an intuitive JavaFX interface.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [System Requirements](#system-requirements)

## Features

✨ **User Authentication**
- Secure login and account creation
- Email validation (Gmail required)
- Password strength requirements (minimum 6 characters)
- Persistent user storage

📝 **Resume Building**
- Personal Information (name, contact, social profiles)
- Education details (degree, institution, CGPA)
- Work Experience with date tracking
- Skills, Projects, Publications
- Certifications with issuing authority
- Languages and Hobbies

📄 **PDF Generation**
- Professional formatting with page borders
- Profile picture support
- Clickable hyperlinks (LinkedIn, GitHub, Email)
- Page numbers and footer
- Organized sections with tables

🎨 **User Interface**
- Clean, intuitive JavaFX design
- File chooser for profile pictures
- Date pickers for all date fields
- Real-time validation
- Responsive scroll panels

## Technologies

| Technology | Purpose |
|-----------|---------|
| **JavaFX** | GUI framework |
| **iTextPDF** | PDF generation |
| **Jackson** | JSON data persistence |

## Installation

### Prerequisites
- Java Development Kit (JDK) 11 or higher
- JavaFX SDK 23.0.1
- Maven or manual JAR management

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/ThrishaRajesh/Resume_Builder.git
   cd Resume_Builder
   ```

2. **Download JavaFX SDK**
   - Download [JavaFX 23.0.1](https://gluonhq.com/products/javafx/)
   - Extract and note the path

3. **Compile and Run**
   ```bash
   javac -cp "lib/*:src" src/*.java
   
   java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml -cp "lib/*:src" ResumeBuilder
   ```

   Or configure your IDE with JavaFX settings.

## Usage

### Getting Started

1. **Launch the application** - The login page appears
2. **Create an Account** - Click "Create Account" and fill in:
   - Username
   - Email (must be @gmail.com)
   - Password (minimum 6 characters)
3. **Login** - Use your credentials to access the resume builder
4. **Fill Resume Details** - Complete all sections:
   - Personal Information
   - Education
   - Experience (optional)
   - Skills, Projects, Publications
   - Certifications, Languages, Hobbies
5. **Upload Profile Picture** - Optional profile photo
6. **Generate PDF** - Click "Generate PDF" to create your resume

### Output

Generated PDFs are saved as `Resume_[YourName].pdf` in the project root directory.

## Project Structure

```
Resume_Builder/
├── src/
│   ├── ResumeBuilder.java      # Main application & GUI
│   ├── ResumeData.java          # Data model for resume
│   ├── PDFGenerator.java        # PDF creation logic
│   └── UserData.java            # User authentication & storage
├── lib/
│   ├── javafx.properties        # JavaFX configuration
│   └── [dependency JARs]
├── resources/
│   └── styles.css               # GUI styling
├── users.json                   # User database
└── README.md
```

### Key Classes

**ResumeBuilder.java**
- Manages the JavaFX application lifecycle
- Handles login and account creation UI
- Controls the resume form and PDF generation

**ResumeData.java**
- Data model storing all resume information
- Getters and setters for each resume field

**PDFGenerator.java**
- Converts ResumeData to formatted PDF
- Applies styling, borders, and hyperlinks
- Creates organized sections and tables

**UserData.java**
- Loads/saves user credentials from `users.json`
- Uses Jackson ObjectMapper for serialization

## System Requirements

- **OS**: Windows, macOS, Linux
- **Java**: JDK 11+
- **RAM**: 512 MB minimum
- **Disk Space**: 100 MB
- **Display**: Minimum 1024x768 resolution

## License

This project is open source and available under the MIT License.

## Author

**Thrisha Rajesh**

---

**Happy Resume Building!** 🚀
