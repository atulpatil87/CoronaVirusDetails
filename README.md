# Corona Details - COVID-19 Tracker

This project is a **Java-based GUI application** that fetches and displays real-time COVID-19 statistics for any country using data scraped from the **Worldometer** website. The application uses the **Swing library** for the graphical interface and **Jsoup** for web scraping.

---

## Features

- **Real-Time Data**: Fetches live COVID-19 statistics, including total cases, deaths, and recoveries.
- **Simple GUI**: User-friendly interface for inputting country names and viewing data.
- **Dynamic Updates**: Automatically retrieves the latest data from the Worldometer website.
- **HTML Display**: Formats the data using HTML for better readability.

---

## Technologies Used

- **Java**: Core language used for building the application.
- **Swing**: For creating the graphical user interface.
- **Jsoup**: For web scraping to extract data from the Worldometer website.
- **AWT**: Used for layout management in the GUI.

---

## Prerequisites

1. **Java Development Kit (JDK)** installed (version 8 or above).
2. **Internet Connection** to fetch real-time data.
3. Add the **Jsoup library** to your project:
   - Download Jsoup from [https://jsoup.org/download](https://jsoup.org/download).
   - Add the jar file to your project's classpath.

---

## How to Run the Application

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```
2. **Set Up the Environment**:
   - Ensure JDK is installed and configured.
   - Add the `jsoup-<version>.jar` file to your project.
3. **Compile the Code**:
   ```bash
   javac CoronaDetails.java
   ```
4. **Run the Application**:
   ```bash
   java CoronaDetails
   ```

---

## How It Works

1. The user inputs the name of a country (e.g., "India") in the text field.
2. On clicking the **"Get"** button:
   - The program constructs a URL for the Worldometer page corresponding to the input country.
   - **Jsoup** connects to the page and scrapes the COVID-19 statistics (total cases, deaths, recoveries).
   - The data is formatted as HTML and displayed in the GUI.
3. The results are displayed in a central label within the application window.

---

## Code Overview

### 1. `getData` Method
- **Purpose**: Fetch and format COVID-19 statistics for a specified country.
- **Process**:
  - Connect to the Worldometer page for the country.
  - Extract data using HTML selectors.
  - Format the data into an HTML string for display.

### 2. GUI Setup
- Components:
  - **`JFrame`**: Main application window.
  - **`JTextField`**: Input field for the country name.
  - **`JLabel`**: Displays the retrieved data.
  - **`JButton`**: Fetches data when clicked.
- **Layout**: Arranged using `BorderLayout` (North-Center-South).

---

## Example Output

1. **Input**: "India"
2. **Output**:
   ```html
   INDIA
   Coronavirus Cases: 34,567,890
   Deaths: 456,789
   Recovered: 33,456,123
   ```

---

## Possible Enhancements

1. **Error Handling**:
   - Display a user-friendly message for invalid input or network errors.
2. **Global Data**:
   - Add functionality to fetch global COVID-19 statistics.
3. **Improved UI**:
   - Enhance the GUI with better styling and responsiveness.
4. **Data Caching**:
   - Cache recent queries to reduce repeated requests.

---

## License

This project is open-source and free to use under the [MIT License](LICENSE).

---

## Acknowledgments

- Data sourced from [Worldometer](https://www.worldometers.info/coronavirus/).
- Developed using the **Jsoup** library for web scraping.
