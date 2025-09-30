#include <stdio.h>

// Define structure
struct Student {
    char name[50];
    int roll;
    float marks[5];   // marks in 5 subjects
    float total;
    float average;
};

int main() {
    struct Student s;
    int i;

    // Input student details
    printf("Enter student name: ");
    scanf("%s", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.roll);

    s.total = 0;

    // Input marks for 5 subjects
    printf("Enter marks in 5 subjects:\n");
    for (i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%f", &s.marks[i]);
        s.total += s.marks[i];
    }

    // Calculate average
    s.average = s.total / 5.0;

    // Output result
    printf("\n--- Student Report ---\n");
    printf("Name: %s\n", s.name);
    printf("Roll No: %d\n", s.roll);
    printf("Total Marks: %.2f\n", s.total);
    printf("Average Marks: %.2f\n", s.average);

    if (s.average >= 50)
        printf("Result: PASS\n");
    else
        printf("Result: FAIL\n");

    return 0;
}