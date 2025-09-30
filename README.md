uct Student {
    char name[20];
    int roll, m1, m2, m3, total;
    float avg;
};
int main() {
    struct Student s;
    printf("Enter name, roll, 3 subject marks:\n");
    scanf("%s %d %d %d %d", s.name, &s.roll, &s.m1, &s.m2, &s.m3);
    s.total = s.m1 + s.m2 + s.m3;
    s.avg = s.total / 3.0;
    printf("\nName: %s\nRoll: %d\nTotal: %d\nAverage: %.2f\n", s.name, s.roll, s.total, s.avg);
    return
