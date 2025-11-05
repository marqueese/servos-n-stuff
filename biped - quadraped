import time

# -------------------------------
# Simulated robot movement system
# -------------------------------

class Robot:
    def __init__(self):
        self.position = 0
        self.rotation = 0
        self.mode = "car"

    def walk_forward(self):
        print("Walking forward...")
        self.position += 230
        time.sleep(0.5)
        print(f"Position: {self.position}")

    def walk_backward(self):
        print("Walking backward...")
        self.position -= 270
        time.sleep(0.5)
        print(f"Position: {self.position}")

    def turn_left(self):
        print("Turning left...")
        self.rotation -= 90
        time.sleep(0.5)
        print(f"Rotation: {self.rotation}°")

    def turn_right(self):
        print("Turning right...")
        self.rotation += 90
        time.sleep(0.5)
        print(f"Rotation: {self.rotation}°")

    def align_bot(self):
        print("Aligning bot...")
        time.sleep(0.5)
        print("Bot aligned.")

    def become_biped(self):
        self.mode = "biped"
        print("Switching to biped mode...")
        time.sleep(1)
        print("Now standing upright.")

    def become_car(self):
        self.mode = "car"
        print("Switching to car mode...")
        time.sleep(1)
        print("Now in car mode.")

# -------------------------------
# Controller simulation
# -------------------------------

class Controller:
    def __init__(self, robot):
        self.robot = robot

    def button_pressed(self, button):
        """Simulate pressing a controller button."""
        actions = {
            'L1': self.robot.walk_forward,
            'L2': self.robot.walk_backward,
            'R1': self.robot.turn_right,
            'R2': self.robot.turn_left,
            'A': self.robot.become_biped,
            'B': self.robot.become_car,
            'X': self.robot.align_bot,
        }
        action = actions.get(button)
        if action:
            action()
        else:
            print(f"Button {button} does nothing.")

# -------------------------------
# Main program
# -------------------------------

def main():
    robot = Robot()
    controller = Controller(robot)

    print("Robot ready! Waiting for inputs...")

    # Example of manual control flow:
    controller.button_pressed('L1')# walk forward
    controller.button_pressed('R1')# turn right
    controller.button_pressed('A')# become biped
    controller.button_pressed('L2')# walk backward
    controller.button_pressed('B')# become car
    controller.button_pressed('X')# align bot

if __name__ == "__main__":
    main()
