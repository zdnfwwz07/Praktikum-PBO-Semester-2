# Praktikum-PBO-Semester-2

## Kegiatan 1
class LightSwitch():
    def __init__(self):
        self.switchIsOn = False

    def turnOn(self):
        # turn the switch on
        self.switchIsOn = True

    def turnOff(self):
        # turn the switch off
        self.switchIsOn = False

    def show(self):  # added for testing
        print(self.switchIsOn)


# Main code
oLightSwitch = LightSwitch()

# Calls to methods
oLightSwitch.show()
oLightSwitch.turnOn()
oLightSwitch.show()
oLightSwitch.turnOff()
oLightSwitch.show()
oLightSwitch.turnOn()
oLightSwitch.show()

## Kegiatan 2
class LightSwitch():
    def __init__(self):
        self.switchIsOn = False

    def turnOn(self):
        # turn the switch on
        self.switchIsOn = True

    def turnOff(self):
        # turn the switch off
        self.switchIsOn = False

    def show(self):  # added for testing
        print(self.switchIsOn)


# Main code
oLightSwitch1 = LightSwitch()
oLightSwitch2 = LightSwitch()

# Test code
oLightSwitch1.show()
oLightSwitch2.show()

oLightSwitch1.turnOn()  # Turn switch 1 on

# Switch 2 should be off at start, but this makes it clearer
oLightSwitch2.turnOff()

oLightSwitch1.show()
oLightSwitch2.show()

## Kegiatan 3
class RemoteTv():

    def __init__(self):
        self.switchIsOn = False
        self.brightness = 0

    def turnOn(self):
        self.switchIsOn = True

    def turnOff(self):
        self.switchIsOn = False

    def raiseLevel(self):
        if self.brightness < 10:
            self.brightness = self.brightness + 1

    def lowerLevel(self):
        if self.brightness > 0:
            self.brightness = self.brightness - 1

    # Extra method for debugging
    def show(self):
        print('Switch is on ?', self.switchIsOn)
        print('Brightness is:', self.brightness)


# Main code
remoteSatu = RemoteTv()

# Turn switch on, and raise the level 5 times
remoteSatu.turnOn()
remoteSatu.raiseLevel()
remoteSatu.raiseLevel()
remoteSatu.raiseLevel()
remoteSatu.raiseLevel()
remoteSatu.raiseLevel()
remoteSatu.show()

# Lower the level 2 times, and turn switch off
remoteSatu.lowerLevel()
remoteSatu.lowerLevel()
remoteSatu.turnOff()
remoteSatu.show()

## Kegiatan 4
class RemoteTv():

    def __init__(self):
        self.switchIsOn = False
        self.brightness = 0
        self.volume = 0   # tambahan atribut volume

    def turnOn(self):
        self.switchIsOn = True

    def turnOff(self):
        self.switchIsOn = False

    def raiseLevel(self):
        if self.brightness < 10:
            self.brightness += 1

    def lowerLevel(self):
        if self.brightness > 0:
            self.brightness -= 1

    # Method tambahan untuk volume
    def volumeUp(self):
        if self.volume < 20:
            self.volume += 1

    def volumeDown(self):
        if self.volume > 0:
            self.volume -= 1

    # Method untuk melihat status
    def show(self):
        print("Switch is on ?", self.switchIsOn)
        print("Brightness is:", self.brightness)
        print("Volume is:", self.volume)


# Main code
remoteSatu = RemoteTv()

remoteSatu.turnOn()
remoteSatu.volumeUp()
remoteSatu.volumeUp()
remoteSatu.volumeUp()
remoteSatu.show()

remoteSatu.volumeDown()
remoteSatu.turnOff()
remoteSatu.show()
