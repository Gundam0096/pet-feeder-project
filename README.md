# pet-feeder-project
This project is an intelligent automated pet feeding system designed to dispense food at scheduled times while monitoring food levels and bowl weight. It ensures your pet is fed reliably and alerts you if any issues occur, such as an empty food container or failed dispensing.


IF FeedingTime == 8 OR FeedingTime == 18 THEN
    IF FoodLevel > 0 THEN
        IF BowlWeight == 0 THEN
            RotateMotor()
            WAIT 5 seconds
            IF BowlWeight == 0 THEN
                SendAlert("Food not dispensed properly.")
            ENDIF
        ELSE
            SendAlert("Bowl already has food.")
        ENDIF
    ELSE
        SendAlert("Food level is empty.")
    ENDIF
ENDIF

