# **Weather Tracker**
The Weather Tracker is a Go-based application that retrieves real-time weather information from a public API, providing current weather data for a specified location. The project leverages Go’s simplicity and performance to fetch and display weather updates.

## **Project Structure**
```
weather-tracker/
│
├── main.go
├── README.md
└── .env (not included in the repository, contains sensitive API key)
```
## **Features**
- **Weather Information Retrieval**: Fetches current weather details such as temperature, humidity, and general weather conditions.
- **User Input**: Allows users to specify the city for which they want to retrieve weather information.
- **API Integration**: Utilizes a public weather API to collect real-time data.
## **Installation and Setup**
### 1. **Clone the Repository**
```bash
git clone https://github.com/MikeOnBoard/weather-tracker.git
cd weather-tracker
```
### 2. **Set Up Your Environment**
Ensure Go is installed on your machine, then run:

```bash
go mod tidy
```
### 3. **Configure API Access**
You will need an API key from a weather service (e.g., OpenWeatherMap).

1. Visit OpenWeatherMap and create an account to get your API key.
2. Create a ``.env`` file in the root directory:
```makefile
Copiar código
API_KEY=your_api_key
```
### 4. **Running the Application**
Run the application with:

```bash
go run main.go
```
When prompted, enter the name of a city to get the current weather:

```mathematica
Enter city: New York
```
The application will return the weather data for the specified city.

## **File Overview**
### **``main.go``**
- **Purpose**: The main file that handles fetching and displaying weather data.
- **Core Functionality**:
  - Retrieves the API key from the environment.
  - Accepts user input for the city name.
  - Sends a request to the weather API and parses the response.
  - Displays weather information such as temperature, weather conditions, and more.
### **Key Functions**:
- ``main()``: The entry point of the application. Handles user input and the process of fetching and displaying weather data.
- ``getWeatherData()``: Communicates with the weather API to retrieve data.
- ``formatWeatherData()``: Formats and prints the weather information in a user-friendly format.
### **Environment Configuration**
The application uses environment variables to securely handle the API key.

1. Ensure the ``.env`` file is set up with the following:
```makefile
API_KEY=your_api_key
```
### **API Reference**
The application interacts with the public weather API (such as OpenWeatherMap). You need an API key to use their service.

- **Endpoint**: ``https://api.openweathermap.org/data/2.5/weather``
- **Request Parameters**:
  - ``q``: City name (required)
  - ``appid``: API key (required)
  - ``units``: Unit of measurement (optional, defaults to metric)
### **Usage Example**
After running the program, you will be prompted to input a city:

```bash
Enter city: Tokyo
```
Output:

```css
City: Tokyo
Temperature: 25.3°C
Weather: Clear sky
Humidity: 50%
```
## **Conclusion**
The Weather Tracker is a simple, yet effective, tool for fetching real-time weather updates for any city worldwide. By utilizing a public weather API, this application provides an accessible way to track weather conditions, making it useful for both developers exploring API interactions and users wanting quick weather data.