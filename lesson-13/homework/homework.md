### Task 1

1. **Database Creation**:
   - Create a new SQLite database named `roster.db`.
   - Define a table called **Roster** with the following schema:
     - **Name**: TEXT
     - **Species**: TEXT
     - **Age**: INTEGER

2. **Insert Data**:
   - Populate the **Roster** table with the following entries:

| Name           | Species  | Age |
|----------------|----------|-----|
| Benjamin Sisko | Human    | 40  |
| Jadzia Dax     | Trill    | 300 |
| Kira Nerys     | Bajoran  | 29  |

3. **Update Data**:
   - Update the `Name` of **Jadzia Dax** to **Ezri Dax**.

4. **Query Data**:
   - Retrieve and display the **Name** and **Age** of all characters where the `Species` is **Bajoran**.

5. **Delete Data**:
   - Remove all characters aged over 100 years from the table.

6. **Bonus Task**:
   - Add a new column called `Rank` to the **Roster** table and update the data with the following values:
   
| Name           | Rank       |
|----------------|------------|
| Benjamin Sisko | Captain    |
| Ezri Dax       | Lieutenant |
| Kira Nerys     | Major      |

7. **Advanced Query**:
   - Retrieve all characters sorted by their `Age` in descending order.

---

### Task 2

Scrape weather information from an HTML file and process it using Python and BeautifulSoup.

<h4>5-Day Weather Forecast</h4>
<table>
    <thead>
        <tr>
            <th>Day</th>
            <th>Temperature</th>
            <th>Condition</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Monday</td>
            <td>25°C</td>
            <td>Sunny</td>
        </tr>
        <tr>
            <td>Tuesday</td>
            <td>22°C</td>
            <td>Cloudy</td>
        </tr>
        <tr>
            <td>Wednesday</td>
            <td>18°C</td>
            <td>Rainy</td>
        </tr>
        <tr>
            <td>Thursday</td>
            <td>20°C</td>
            <td>Partly Cloudy</td>
        </tr>
        <tr>
            <td>Friday</td>
            <td>30°C</td>
            <td>Sunny</td>
        </tr>
    </tbody>
</table>


Assume you are given the following HTML structure (you can save it as `weather.html`):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Weather Forecast</title>
</head>
<body>
    <h4>5-Day Weather Forecast</h4>
    <table>
        <thead>
            <tr>
                <th>Day</th>
                <th>Temperature</th>
                <th>Condition</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Monday</td>
                <td>25°C</td>
                <td>Sunny</td>
            </tr>
            <tr>
                <td>Tuesday</td>
                <td>22°C</td>
                <td>Cloudy</td>
            </tr>
            <tr>
                <td>Wednesday</td>
                <td>18°C</td>
                <td>Rainy</td>
            </tr>
            <tr>
                <td>Thursday</td>
                <td>20°C</td>
                <td>Partly Cloudy</td>
            </tr>
            <tr>
                <td>Friday</td>
                <td>30°C</td>
                <td>Sunny</td>
            </tr>
        </tbody>
    </table>

</body>
</html>
```

1. **Parse the HTML File**:
   - Load the `weather.html` file using BeautifulSoup and extract the weather forecast details.

2. **Display Weather Data**:
   - Print the **day**, **temperature**, and **condition** for each entry in the forecast.

3. **Find Specific Data**:
   - Identify and print the day(s) with:
     - The highest temperature.
     - The "Sunny" condition.

4. **Calculate Average Temperature**:
   - Compute and print the **average temperature** for the week.

---

### Task 3

Scrape job listings from the website https://realpython.github.io/fake-jobs and store the data into an SQLite database.

1. **Scraping Requirements**:
   - Extract the following details for each job listing:
     - **Job Title**
     - **Company Name**
     - **Location**
     - **Job Description**
     - **Application Link**

2. **Data Storage**:
   - Store the scraped data into an SQLite database in a table named `jobs`.

3. **Incremental Load**:
   - Ensure that your script performs **incremental loading**:
     - Scrape the webpage and add only **new job listings** to the database.
     - Avoid duplicating entries. Use `Job Title`, `Company Name`, and `Location` as unique identifiers for comparison.

4. **Update Tracking**:
   - Add functionality to detect if an existing job listing has been updated (e.g., description or application link changes) and update the database record accordingly.

5. **Filtering and Exporting**:
   - Allow filtering job listings by **location** or **company name**.
   - Write a function to export filtered results into a CSV file.
