# Technical Overview

This repository is intended to host and manage modified versions of third-party libraries used for PDF and document generation, such as `mpdf`. Only essential parts of each library will be retained to reduce repository size and improve maintainability. The actual application/plugin code will reside separately.

## Purpose

The repository is created to:

- Maintain only the required portions of third-party libraries (after customization or cleanup).
- Ensure any user can access and download the library code easily.
- Provide a clean, lightweight version of the libraries to be used in the main plugin.

---

## Included Libraries

### 📦 `mpdf` (Currently Used)

**Initial Setup and Customization Process:**

1. **Install via Composer:**

   Download and install the `mpdf` library using Composer in a temporary directory:

   ```bash
   composer require mpdf/mpdf
   ```

2. **Reduce Font Size:**

   Navigate to the `./ttfonts` directory inside the `vendor/mpdf/mpdf/ttfonts` folder and **delete all contents** except:

   - `DejaVuSans-Bold.ttf`  
     *(Optional: This is kept as the default font and can be removed if not required.)*

3. **Clean & Commit:**

   - Retain only the relevant files and directories needed for the plugin.
   - Push the cleaned-up version to the repository.

---

## Library Update Instructions

Whenever an update is required for the libraries, follow these steps:

1. **Install the latest version** of the library via Composer.
2. **Apply the same cleanup rules** (e.g., remove unused fonts, unneeded files).
3. **Test integration** with the plugin to ensure compatibility.
4. **Replace the existing library files** in the repository.
5. **Update this document** if any changes in the modification steps are required.

---

## Notes

- This repository is meant to be **public** so that other developers or users can freely download the modified libraries.
- The core business logic, plugin-specific integration, and other application code will **not be included here** — it resides in the main plugin repository.
