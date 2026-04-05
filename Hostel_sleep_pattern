import random
import statistics

class Student:
    def __init__(self, name):
        self.name = name
        self.sleep_times = []
        self.wake_times = []

    def log_sleep(self, sleep_hour, wake_hour):
        self.sleep_times.append(sleep_hour)
        self.wake_times.append(wake_hour)

    def average_sleep(self):
        durations = []
        for s, w in zip(self.sleep_times, self.wake_times):
            if w < s:
                w += 24
            durations.append(w - s)
        return round(statistics.mean(durations), 2)

    def __str__(self):
        return f"{self.name}: Avg Sleep = {self.average_sleep()} hrs"


class Hostel:
    def __init__(self, name):
        self.name = name
        self.students = []

    def add_student(self, student):
        self.students.append(student)

    def simulate_week(self):
        for _ in range(7):
            for student in self.students:
                sleep = random.randint(21, 26) % 24  # 9 PM to 2 AM
                wake = random.randint(5, 9)          # 5 AM to 9 AM
                student.log_sleep(sleep, wake)

    def report(self):
        print(f"\nSleep Report for {self.name}")
        print("-" * 40)
        for student in self.students:
            print(student)

    def overall_average(self):
        all_sleep = []
        for s in self.students:
            all_sleep.append(s.average_sleep())
        return round(statistics.mean(all_sleep), 2)


def generate_students(n):
    return [Student(f"Student_{i+1}") for i in range(n)]


def sleep_distribution(hostel):
    distribution = {"<5 hrs": 0, "5-7 hrs": 0, "7+ hrs": 0}
    for s in hostel.students:
        avg = s.average_sleep()
        if avg < 5:
            distribution["<5 hrs"] += 1
        elif avg <= 7:
            distribution["5-7 hrs"] += 1
        else:
            distribution["7+ hrs"] += 1
    return distribution


def print_distribution(dist):
    print("\nSleep Distribution:")
    for k, v in dist.items():
        print(f"{k}: {v} students")


def debug_student(student):
    print(f"\nDebugging {student.name}")
    print("Sleep Times:", student.sleep_times)
    print("Wake Times:", student.wake_times)


def main():
    hostel = Hostel("Sunrise Hostel")
    students = generate_students(15)

    for s in students:
        hostel.add_student(s)

    hostel.simulate_week()
    hostel.report()

    avg = hostel.overall_average()
    print("\nOverall Avg Sleep:", avg, "hrs")

    dist = sleep_distribution(hostel)
    print_distribution(dist)

    debug_student(students[0])


if __name__ == "__main__":
    main()
