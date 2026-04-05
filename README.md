# Student-study-hr-sleeping-hr

🏨 Hostel Sleep Pattern Analysis (Python Project)

📌 Overview

This project simulates and analyzes the sleep patterns of students living in a hostel. It generates random sleep and wake times for each student over a week and computes useful statistics such as average sleep duration and overall hostel sleep trends.

The program is designed using object-oriented programming concepts in Python and demonstrates data simulation, analysis, and reporting.

---

🚀 Features

- Simulates sleep behavior of multiple students
- Calculates individual average sleep duration
- Computes overall hostel average sleep
- Categorizes students based on sleep duration:
  - Less than 5 hours
  - Between 5 to 7 hours
  - More than 7 hours
- Debug feature to inspect individual student data
- Uses Python standard libraries ("random", "statistics")

---

🧱 Project Structure

- Student Class
  
  - Stores sleep and wake times
  - Computes average sleep duration

- Hostel Class
  
  - Manages multiple students
  - Simulates weekly sleep patterns
  - Generates reports and averages

- Utility Functions
  
  - "generate_students(n)" → Creates student objects
  - "sleep_distribution(hostel)" → Categorizes sleep patterns
  - "print_distribution(dist)" → Displays distribution
  - "debug_student(student)" → Prints raw data for debugging

---

⚙️ How It Works

1. Students are created and added to a hostel
2. Sleep and wake times are randomly generated for 7 days:
   - Sleep: 9 PM to 2 AM
   - Wake: 5 AM to 9 AM
3. Sleep duration is calculated:
   - If wake time is less than sleep time, it assumes overnight sleep
4. Averages and distributions are computed and displayed

---

▶️ How to Run

1. Make sure Python is installed (Python 3.x)
2. Save the code in a file (e.g., "sleep_analysis.py")
3. Run the program:

python sleep_analysis.py

---

📊 Sample Output

- Individual student sleep averages
- Overall hostel average sleep
- Sleep distribution summary
- Debug details of one student

---

🧠 Concepts Used

- Object-Oriented Programming (OOP)
- Lists and loops
- Random data generation
- Statistical analysis (mean)
- Conditional logic

---

⚠️ Notes

- Output varies every time due to random data generation
- Sleep crossing midnight is handled correctly
- Designed for educational and simulation purposes

---

🔮 Future Enhancements

- Add graphical visualization (charts using matplotlib)
- Store data in files (CSV/Database)
- Build a GUI interface using Tkinter
- Add real-time tracking instead of random simulation

---

👨‍💻 Author

G. Sudeep Narayana

---

📄 License

This project is for educational purposes and free to use.
