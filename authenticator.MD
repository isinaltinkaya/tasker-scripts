## Auto-Authenticator: Make authentication easier (and unsafe!)

Trying to live and work in peace in a world full of unnecessary security/safety measures. 

- Requires root.

- Use at your own risk. (I mean really, it may even be illegal in some cases)

- Tested on LineageOS 18.1 + Magisk + Root + Tasker 5.14.6


### Variables

- AUTHENTICATION-APP
- X : Screen tap X coordinate
- Y : Screen tap Y coordinate

### How to

1. Turn on the screen touch coordinates using the Developer options.
2. Determine the X and Y values of the buttons you need to touch.
3. Adjust the waiting times.


### Code snipped
```  
    Profile: EXAMPLE
    Settings: Restore: no
        Event: Notification [ Owner Application:AUTHENTICATION-APP Title:* Text:* Subtext:* Messages:* Other Text:* Cat:* New Only:On ]


    Enter Task: auto-auth

    Task: auto-auth

    A1: Launch App [
         Package/App Name: AUTHENTICATION-APP ]

    A2: Wait [
         MS: 0
         Seconds: 3
         Minutes: 0
         Hours: 0
         Days: 0 ]

    A3: Run Shell [
         Command: input tap X Y
         Timeout (Seconds): 0
         Use Root: On ]

    A4: Run Shell [
         Command: input tap X Y
         Timeout (Seconds): 0
         Use Root: On ]

    A5: Run Shell [
         Command: input tap X Y
         Timeout (Seconds): 0
         Use Root: On ]

    A6: Run Shell [
         Command: input tap X Y
         Timeout (Seconds): 0
         Use Root: On ]

    A7: Run Shell [
         Command: input tap X  Y
         Timeout (Seconds): 0
         Use Root: On ]

    A8: Run Shell [
         Command: input tap X Y
         Timeout (Seconds): 0
         Use Root: On ]

    A9: Wait [
         MS: 0
         Seconds: 5
         Minutes: 0
         Hours: 0
         Days: 0 ]

    A10: Run Shell [
          Command: input tap X Y
          Timeout (Seconds): 0
          Use Root: On ]

    A11: Wait [
          MS: 0
          Seconds: 3
          Minutes: 0
          Hours: 0
          Days: 0 ]

    A12: Kill App [
          App: AUTHENTICATION-APP
          Use Root: On ]
```
