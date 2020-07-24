# Teamcode Organization

### Subsystem Organization
* One useful way to organize your code is with a subsystem organization — essentially, we are breaking down the robot into respective hardware classes. 
  *For example, for a mecanum drive train, we have one OpMode. In this example, that is Drive.java. By separating hardware into classes like this, we can test each piece of hardware separately - for example, we can test the drivetrain even when the lift is not ready to test. 

* As you can see here, in Drive.java, we are creating a MecanumDrive object, which is our subsystem. Now, we can make use of MecanumDrive.java’s methods, like init(), controller(), getLFrontPower(), getLFrontVelocity(), etc. We also have a similar Lift subsystem, so you can see that I used this subsystem to create a lift object in Drive as well. 

* Another useful class to have is a Constants.java class, containing constants that are useful for all classes. 

* Subsystems allow for more consistency and greater efficiency, encouraging abstraction and code reuse. All op modes use the same consistent interface for interacting with the robot subsystems, and all of the logic for managing the systems is in one place. For example, if you are trying to make a new autonomous opmode program, with subsystem organization, you can easily call the subsystems in that program, instead of copying and pasting all your methods into each new program.

### .xml Configuration
* Another structure our teams are learning to implement are .xml configurations. Instead of having to enter every motor, servo, and sensor configuration from scratch on the robot controller phone, by creating an .xml configuration in Android Studio and loading it into the phone along with the rest of your code, managing your hardware map is a lot more efficient. As long as your team is regularly backing up your code, your existing .xml configuration can also be restored if you were to lose it.


* We learned this method from a TNT, team 9929, coach, so we thought we would share it with you all as well. [9929's Website](https://ftc9929.com/2019/12/16/stress-free-ftc-hardware-configurations/
)
