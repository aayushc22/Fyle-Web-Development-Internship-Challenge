# Tax-Calculator

This tool helps you figure out how much money you'll have left after paying taxes. It takes into account your main income, any extra money you make, your age group, and any deductions you can claim.

# How it works

Input Your Income: First, you tell the calculator how much you earn in a year. This includes your salary from your job.
Extra Income: If you have any additional income from side gigs or investments, you can add that too.
Age Group: You select your age group. This helps determine the tax rules that apply to you.
Deductions: You can enter any tax deductions you're eligible for. This reduces the amount of income you're taxed on.
Submit: After filling in the details, you hit the submit button.

# What you get

The calculator crunches the numbers and shows you how much money you'll have left after taxes. It considers everything you've entered to give you an accurate estimate.

## References & Requirements

- The tax calculation works based on this formula -
  - Overall income (after deductions) under 8 (≤) Lakhs is not taxed.
    - Ex - if Gross Annual Income + Extra Income - Deductions = 6 Lakhs, no tax
    - if Gross Annual Income + Extra Income - Deductions = 9 Lakhs, tax
  - Income over 8 (>) Lakhs, the amount over 8 Lakhs is taxed at
    - 30% for people with age < 40
    - 40% for people with age ≥ 40 but < 60
    - 10% for people with age ≥ 60
    - Example
      - Age = 34, Income = 40 Lakhs, no deductions, tax = .3 _ (40 - 8) = .3 _ 32 = 9.6 Lakhs
- Do not restrict the user from entering incorrect values like characters in the number fields
  - Highlight an error icon to the right of the input field (shown as an example in the above image as a circle with `!`). Hovering over it should show the error in a tooltip
  - If no errors are present, don't show the error icon
  - This should be present in all the number fields
- The age dropdown field should have 3 values -
  - <40
  - ≥ 40 & < 60
  - ≥ 60
  - If the user has not entered this value and clicks on submit, show an error icon hovering over which should show that the input field is mandatory
- Error icons should not be visible in the form by default.
- Clicking on submit should show a modal which would show the final values based on the above calculations.

# Assumptions Considered:

Input Validation:

We've implemented thorough input validation to ensure accurate data processing:

    Validation Triggers: Input values are checked for validity when you focus on them, make changes, or click the submit button.

    Error Display:
        Negative Numbers: If you type a number less than zero, you'll see an error message reminding you to input non-negative numbers.
        Empty Fields: Leaving any field empty or not typing anything before submission triggers an error message indicating the field is mandatory.
        Non-Numeric Input: If you type anything other than a number, a message pops up asking you to input numbers only.

# Overall Income Calculation:

We've set up the calculation process to be intuitive:

    Income Threshold: If the combined total of gross income, extra income, and deductions doesn't exceed 8 lakhs, the overall income displayed will be the sum of your gross income and extra income.

These assumptions streamline the user experience, ensuring accurate data entry and clear understanding of the results.

# How to Run

Step 1 : Download the Code:

    Start by downloading the HTML, CSS, and JavaScript files to your computer. You can do this by clicking on the provided download link or by copying the code and saving it into separate files with the corresponding file extensions (.html, .css, .js).

Step 2 : Open HTML File:

    After downloading, locate the HTML file you've downloaded and open it in your preferred web browser. You can do this by double-clicking the HTML file or by right-clicking and selecting "Open with" and then choosing your web browser from the list.

Step 3 : Ensure Internet Connection:

    It's important to ensure that your computer is connected to the internet while running the application locally. This is because the application uses Bootstrap icons via CDN links. If you're offline, these icons may not appear.

Step 4 : Interact with the Application:

    Once the HTML file is open in your web browser, you can interact with the tax calculator just as you would on a live website. Input values into the fields, click the submit button, and observe how the calculations and error messages behave

## Test Cases

**Test Case 1: When users hover over the question mark icons, tooltips will be displayed. These tooltips provide additional information regarding the respective fields.**

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/8442eb8f-fe07-4c3d-8ed5-cb3f6c4b98e2" alt="test case 1(tooltip)" width="500"/><br/>

**Test Case 2: In case users input negative values into number fields, error icons will be triggered. These fields exclusively accept non-negative integers. Consequently, an error message will be shown, indicating "Please input non-negative numbers only.**

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/75086cf5-109c-4a6b-a60d-29d889a1dbff" alt="test case 2(Positive Numbers Only)" width="500"/><br/>

**Test Case 3: Upon clicking the submit button without providing any input, error icons will appear. These icons indicate mandatory fields that require user input. The associated error message will be displayed as "This input field is mandatory**<br/>

Image 1: Before
<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/b43e4138-acf0-496b-ae49-bc07029824e7" alt="Test Case 3" width="500"/><br/>
Image 2: After clicking the submit button for empty fields
<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/946895f6-468e-44ab-a15c-c1cd9cf5a091" alt="Test Case 3" width="500"/><br/>

**Test Case 4: Upon clicking the submit button without selecting an age group from the dropdown menu, error icons will appear next to the dropdown. These icons indicate that selecting an age group is mandatory. The associated error message will be displayed as "Select an age group."**

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/d72c880c-b059-4ce7-bad5-8ee91627fd70" alt="test case 4" width="500"/><br/>

**Test Case 5 : Output Results**<br/>
_1. If the sum of Gross Income and Extra Income, minus Total Deductions, is less than or equal to 8 lakhs, then no income tax is applicable. In this case, the overall income will be the sum of Gross Income and Extra Income._

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/283f6c88-03b3-49b6-bc7a-85e74a8fc590" alt="Test Case 5(1)" width="500"/><br/>

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/85ddc308-7def-4cc8-8649-72fe559d0e4e" alt="Test Case 5(1) Result" width="500"/><br/>

_2. Age < 40_
<br/>

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/cda2ea64-9007-4573-ae1b-da697c5adaf1" alt="Test Case 5(2)" width="500"/><br/>

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/2de0a9c7-f9e1-452a-81e1-51ba1737c719" alt="Test Case 5(2) Result" width="500"/><br/>

_3. Age ≥ 40 & < 60_
<br/>
<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/d2b86eb6-4459-44e5-888a-72de41ae1d24" alt="Test Case 5(2)" width="500"/><br/>

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/4a058ff0-b1f8-46b5-af52-212f7c4a87bd" alt="Test Case 5(2) Result" width="500"/><br/>

_4. Age ≥ 60_
<br/>
<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/9c275cb5-bc3d-4cc6-9d7b-a218baa5c75d" alt="Test Case 5(2)" width="500"/><br/>

<img src="https://github.com/ayushtya9i/Fyle-Web-Development-Internship-Challenge/assets/86874794/c181b5c2-64d9-449a-864c-d89141ffca93" alt="Test Case 5(2) Result" width="500"/><br/>
