public class SecondsAndMinutesCalculator {

    public static final String INVALID_VALUE_MESSAGE = "Invalid Value !";
    public static String getDurationString(int minutes, int seconds) {

        if (minutes < 0 || (seconds < 0) || (seconds > 59)) {
            return INVALID_VALUE_MESSAGE;
        }
            int theHour = minutes / 60;
            int getSeconds = minutes % 60;
            return minutes + "minutes " + seconds + "seconds is equal to "
                    + theHour + "h " + getSeconds + "m " + seconds + "s.";

        }

    public static String getDurationString(int seconds) {
        if (seconds < 0) {
            return INVALID_VALUE_MESSAGE;
        }
            int getMinutes = seconds / 60;
            int getSeconds = seconds % 60;
            return seconds + "seconds " + "is equal to " +
                    getMinutes + "minutes " + getSeconds + " seconds";
    }

    public static void main(String[] args) {
        System.out.println(getDurationString(65, 45));
        System.out.println(getDurationString(-3945));              // prints "Invalid Value !"
        System.out.println(getDurationString(234,40));
    }


}
