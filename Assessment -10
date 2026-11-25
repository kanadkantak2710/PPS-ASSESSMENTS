#include <stdio.h>

int main() {
    int year, month, day, startDay, days;
    char *months[] = {
        "January", "February", "March", "April", "May", "June",
        "July", "August", "September", "October", "November", "December"
    };
    int monthDays[] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

    printf("Enter year: ");
    scanf("%d", &year);

    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        monthDays[1] = 29;
    }

    int y = year - 1;
    startDay = (y + y / 4 - y / 100 + y / 400 + 1) % 7;

    for (month = 0; month < 12; month++) {
        days = monthDays[month];

        printf("\n\n  ------------ %s ------------\n", months[month]);
        printf("  Sun  Mon  Tue  Wed  Thu  Fri  Sat\n");

        for (int i = 0; i < startDay; i++) {
            printf("     ");
        }

        for (day = 1; day <= days; day++) {
            printf("%5d", day);

            startDay++;
            if (startDay > 6) {
                startDay = 0;
                printf("\n");
            }
        }
    }

    printf("\n");
    return 0;
}
