class TimerApp:
    def __init__(self, sec, min, hur):
        if sec < 60 and min < 60 and hur <= 24:
            self.sec = sec
            self.min = min
            self.hur = hur
        else:
            raise ValueError("Invalid time values: Ensure sec < 60, min < 60, and hur <= 24")

    def time(self):
        if self.sec >= 60:
            print("Please enter a correct value for seconds")
        if self.min >= 60:
            print("Please enter a correct value for minutes")
        if self.hur > 24:
            print("Please enter a correct value for hours")

    def display_info(self):
        print(f"Time: {self.hur:02d}:{self.min:02d}:{self.sec:02d}")

# Taking user input
sec = int(input("Enter seconds (< 60): "))
min = int(input("Enter minutes (< 60): "))
hur = int(input("Enter hours (≤ 24): "))

# Creating an instance of TimerApp
timer = TimerApp(sec, min, hur)
timer.display_info()
