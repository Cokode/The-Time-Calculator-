# The-Time-Calculator-
This is a project that calculates hours, minutes and seconds based on values received. 

public class SecondsAndMinutesCalculator {

    public static int getDurationString(int minutes, int seconds) {

        if (minutes < 0 || seconds < 0 || seconds > 59) {
            System.out.println("invalid Value !");
            return -1;
        }
            int theHour = minutes / 60;
            int getSeconds = minutes % 60;
            if (minutes > 59) {
            System.out.println(minutes + "minutes " + seconds + "seconds is equal to "
                    + theHour + "h " + getSeconds + "m " + seconds + "s." );
            return theHour;
        } else {
                System.out.println("The time is " + minutes + " minutes " + seconds + " seconds. ");
                return getSeconds;
            }
    }

    public static int getDurationString(int seconds) {
        if (seconds < 0) {
            System.out.println("invalid Value !");
            return -1;
        } else if (seconds >= 60){
            int getMinutes = seconds / 60;
            int getSeconds = seconds % 60;
            System.out.println(seconds + "seconds " + "is equal to " +
                    getMinutes + "minutes " + getSeconds + " seconds");
            return getDurationString(getMinutes, getSeconds);
        } else {
            System.out.println(seconds + "seconds. ");
            return seconds;
        }

    }

    public static void main(String[] args) {
        getDurationString(61, 40);
        getDurationString(400);
        getDurationString(234,40);


    }


}
