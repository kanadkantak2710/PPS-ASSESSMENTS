#include <stdio.h>

float findNearest(float *ptr, int n);

int main() {
    int n, i;
    float distance[100], minDistance;

    printf("Enter the number of sensors: ");
    scanf("%d", &n);

    if (n <= 0 || n > 100) {
        printf("Invalid number of sensors.\n");
        return 1;
    }

    printf("Enter the distance readings (in cm) from %d sensors:\n", n);
    for (i=0;i<n;i++) {
        printf("Sensor %d: ", i+1);
        scanf("%f", &distance[i]);
    }

    minDistance = findNearest(distance, n);

    printf("\nNearest obstacle detected at: %.2f cm\n", minDistance);

    if (minDistance < 20.0) {
        printf("WARNING! Obstacle is too close.\n");
    } else {
        printf("Path is clear.\n");
    }

    return 0;
}

float findNearest(float *ptr, int n) {
    float min = *ptr; 
    int i;

    for (i=1;i<n;i++) {
        if (*(ptr + i) < min) {
            min = *(ptr + i);
        }
    }

    return min;
}
