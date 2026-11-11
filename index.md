Here is the complete code and structure for your assignment (Assignment 4.2 — Job Application Form).

Save the code below into a file named job-application.html. It includes all the required elements: text/email/tel inputs, a date picker for date of birth, a URL input for portfolios, radio buttons with matching names for preferred shifts, checkboxes for skills, a dropdown selection for job roles, a textarea for cover letters, a disabled field example, and a submit button.

File: job-application.html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f6f9;
            margin: 0;
            padding: 2rem 0;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .form-container {
            background: #ffffff;
            padding: 2.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            width: 100%;
            max-width: 600px;
        }
        h2 {
            text-align: center;
            color: #2c3e50;
            margin-top: 0;
            margin-bottom: 1.5rem;
        }
        .form-group {
            margin-bottom: 1.25rem;
        }
        label {
            display: block;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #34495e;
        }
        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        input[type="url"],
        select,
        textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #cbd5e1;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 1rem;
            transition: border-color 0.2s;
        }
        input:focus, select:focus, textarea:focus {
            border-color: #2563eb;
            outline: none;
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }
        input:disabled, select:disabled {
            background-color: #f1f5f9;
            color: #94a3b8;
            cursor: not-allowed;
        }
        .radio-group, .checkbox-group {
            display: flex;
            gap: 1.5rem;
            margin-top: 0.5rem;
            flex-wrap: wrap;
        }
        .radio-item, .checkbox-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-weight: normal;
            color: #475569;
            cursor: pointer;
        }
        .radio-item input, .checkbox-item input {
            cursor: pointer;
        }
        textarea {
            resize: vertical;
            min-height: 100px;
        }
        button[type="submit"] {
            width: 100%;
            background-color: #2563eb;
            color: white;
            padding: 0.75rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.2s;
            margin-top: 1rem;
        }
        button[type="submit"]:hover {
            background-color: #1d4ed8;
        }
    </style>
</head>
<body>

    <div class="form-container">
        <h2>Job Application Form</h2>
        
        <form action="#" method="POST">
            
            <!-- 1. Full Name -->
            <div class="form-group">
                <label for="fullname">Full Name:</label>
                <input type="text" id="fullname" name="fullname" placeholder="John Doe" required>
            </div>

            <!-- 1. Email -->
            <div class="form-group">
                <label for="email">Email Address:</label>
                <input type="email" id="email" name="email" placeholder="john.doe@example.com" required>
            </div>

            <!-- 1. Phone Number -->
            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" placeholder="(123) 456-7890" required>
            </div>

            <!-- 2. Date of Birth -->
            <div class="form-group">
                <label for="dob">Date of Birth:</label>
                <input type="date" id="dob" name="dob" required>
            </div>

            <!-- 3. Portfolio URL -->
            <div class="form-group">
                <label for="portfolio">Portfolio Website URL:</label>
                <input type="url" id="portfolio" name="portfolio" placeholder="https://yourportfolio.com">
            </div>

            <!-- 4. Radio Buttons for Preferred Shift -->
            <div class="form-group">
                <label>Preferred Shift:</label>
                <div class="radio-group">
                    <label class="radio-item"><input type="radio" name="shift" value="morning" required> Morning Shift</label>
                    <label class="radio-item"><input type="radio" name="shift" value="evening"> Evening Shift</label>
                    <label class="radio-item"><input type="radio" name="shift" value="night"> Night Shift</label>
                </div>
            </div>

            <!-- 5. Checkboxes for Skills -->
            <div class="form-group">
                <label>Technical Skills:</label>
                <div class="checkbox-group">
                    <label class="checkbox-item"><input type="checkbox" name="skills" value="html"> HTML & CSS</label>
                    <label class="checkbox-item"><input type="checkbox" name="skills" value="js"> JavaScript</label>
                    <label class="checkbox-item"><input type="checkbox" name="skills" value="python"> Python</label>
                    <label class="checkbox-item"><input type="checkbox" name="skills" value="react"> React</label>
                </div>
            </div>

            <!-- 6. Dropdown for Job Role -->
            <div class="form-group">
                <label for="role">Applying for Job Role:</label>
                <select id="role" name="role" required>
                    <option value="" disabled selected>Select a position</option>
                    <option value="frontend">Frontend Developer</option>
                    <option value="backend">Backend Developer</option>
                    <option value="fullstack">Full-Stack Developer</option>
                    <option value="uiux">UI/UX Designer</option>
                </select>
            </div>

            <!-- Example of a Disabled Field -->
            <div class="form-group">
                <label for="application-id">Application Status (Pre-set):</label>
                <input type="text" id="application-id" name="application_status" value="Draft (New Submission)" disabled>
            </div>

            <!-- 7. Textarea for Cover Letter -->
            <div class="form-group">
                <label for="coverletter">Cover Letter:</label>
                <textarea id="coverletter" name="coverletter" placeholder="Tell us why you are a great fit for this role..."></textarea>
            </div>

            <!-- 8. Submit Button -->
            <button type="submit">Submit Application</button>

        </form>
    </div>

</body>
</html>
How to Complete Your Submission:
Save the File: Save the code above as job-application.html on your computer.

Test the Form: Open job-application.html in your web browser:

Try the date picker, URL field, dropdown role selection, and radio options.

Verify that clicking submit triggers validation on required fields.

Notice the greyed-out Application Status box demonstrating the disabled attribute.

Take a Screenshot: Capture a browser screenshot showing your completed job application form.

Submit: Turn in your job-application.html source file and the screenshot as required by your assignment instructions!