// C program for the above approach
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
// Global variables
char source[20],des[20],train[40];
int CIA;
char station[40], cla[40];
int time1, time2, a[55];
// Defining Structure
struct Rec {
	char name[30];
	char gen[10];
	int Age;
};
int details(int);
int seat(int);
int cal(int, int, int);
int bill(int, int);
// Driver Code
int main()
{
	int i, a1, a2, b, c,x = 0, d, e, r;
	char o;
	printf("Enter Number Of Passengers: ");
	fflush(stdin);
	scanf("%d", &CIA);
	// Calling details() function with argument number of passenger
	details(CIA);
	printf("Note:-Due to current Situation we only serve from Chennai. Sorry for the inconvience\n");
	printf("Enter The Source Place: ");
	fflush(stdin);
	scanf("%s",&source[20]);
	printf("\t\t    Aviable destinations");
	printf("\n");
	printf("-------------------------------------------------\n");
	printf(" S.NO	        Train            Destination     \n");
	printf("-------------------------------------------------\n");
	printf("  1	   Rajdhani Express   Delhi\n");
	printf("  2	   Satabdi Express    Banglore\n");
	printf("  3	   Humsafar Express   Kolkata\n");
	printf("  4	   Kaveri Express     Mysore\n");
	printf("  5	   Duronto Express    Thiruvananthapuram\n");
	printf("-------------------------------------------------\n");

	printf("\n");
	printf("Enter The Destination Place: ");
	fflush(stdin);
	scanf("%s",&des[20]);
	printf("\n");
	printf("----------------------------------------------------------------------------\n");
	printf("The Following Trains Are Available from Chennai due to the Current Situation\n");
	printf("----------------------------------------------------------------------------\n");
    printf("\n");
	printf("---------------------------------------------------------------------------\n");
	printf(" S.NO  Train No.        Train         Departure         Departure Station  \n");
	printf("---------------------------------------------------------------------------\n");
	printf("  1	284531     Rajdhani Express   10:00 a.m     Chennai Central Station\n");
	printf("  2	146437     Satabdi Express    17:00 p.m     Chennai Central Station\n");
	printf("  3	298575     Humsafar Express   23:00 p.m     Chennai Egmore Station \n");
	printf("  4	194834     Kaveri Express     17:00 p.m     Chennai Central Station\n");
	printf("  5     202134     Duronto Express    07:00 a.m     Chennai Central Station\n");
	printf("---------------------------------------------------------------------------\n");

	printf("\n");
	printf("Enter the train in which you wish to travell----> ");
	scanf("%d", &i);
	do {
		switch (i) {
		case 1: {
			strcpy(train,"Rajdhani Express");
			strcpy(station,"Chennai Central Station");
			strcpy(des,"Delhi");
			time1 = 10;
			time2 = 00;
			a1 = 2099;
			a2 = 1560;
			// Calling cal() function with the three argument and return value
			d = cal(a1, a2, CIA);
			printf("Total Bill Amount:%d\n",d);
		}; break;
		case 2: {
			strcpy(train,"Satabdi Express");
			strcpy(station,"Chennai Central Station");
			strcpy(des,"Banglore");
			time1 = 17;
			time2 = 00;
			a1 = 1801;
			a2 = 981;
			// Calling cal() function with the three argument and return value
			d = cal(a1, a2, CIA);
			printf("Total Bill Amount:%d\n",d);
		}; break;
		case 3: {
			strcpy(train,"Humsafar Express");
			strcpy(station,"Chennai Egmore Station");
			strcpy(des,"Kolkata");
			time1 = 23;
			time2 = 00;
			a1 = 2199;
			a2 = 1780;
			// Calling cal() function with the three argument and return value
			d = cal(a1, a2, CIA);
			printf("Total Bill Amount: %d\n", d);
		}; break;
		case 4: {
			strcpy(train, "Kaveri Express");
			strcpy(station, "Chennai Central Station");
			strcpy(des,"Mysore");
			time1 = 17;
			time2 = 00;
			a1 = 1759;
			a2 = 1200;
			// Calling cal() function with the three argument and return value
			d = cal(a1, a2, CIA);
			printf("Total Bill Amount: %d\n", d);
		}; break;
		case 5: {
			strcpy(train, "Duronto Express");
			strcpy(station, "Chennai Central Station");
			strcpy(des,"Thiruvananthapuram");
			time1 = 07;
			time2 = 00;
			a1 = 2205;
			a2 = 1905;
			// Calling cal() function with the three argument and return value
			d = cal(a1, a2, CIA);
			printf("Total Bill Amount: %d\n", d);
		}; break;
		default:
			printf("Enter Correct choice.....\n");
			x = 1;
		}break;
	} while (x);
	printf("Now Book Your Seats......\n");
	// Calling seat() function with number of passenger
	seat(CIA);
	// Calling bill() function with the number of passenger and amount argument
	bill(d, CIA);
}
// Function for calculation of amount
int cal(int y1, int y2, int h)
{
	int b, c, i, t, r, n;
	printf("\t\tEnter Your choice of class--->\n");
	printf("\t\t1. Slepper Class\n");
	printf("\t\t2. A.C Class\n");
	scanf("%d", &i);
	switch (i) {
	case 1: {
		strcpy(cla, "Slepper Class");
		b = y2 * h;
		c = b + (b * 0.18);
	} break;
	case 2: {
		printf("\t\tEnter Your Choice of Tire in\n");
		printf("\t\t1. 1st AC Class\n");
		printf("\t\t2. 2nd AC Class\n");
		printf("\t\t3. 3rd AC Class \n");
		scanf("%d", &n);
		switch (n) {
		case 3: {
			strcpy(cla, "3rd AC Class");
			b = y1 * h;
			c = b + (b * 0.18);
		} break;
		case 2: {
			strcpy(cla, "2nd AC Class");
			b = (y1 + 1000) * h;
			c = b + (b * 0.18);
		} break;
		case 1: {
			strcpy(cla, "1st AC Class");
			b = (y1 + 5000) * h;
			c = b + (b * 0.18);
		} break;
		default: {
			printf("\t\tEnter Right Choice......\n");
		}}} break;
	default: {
		printf("\t\tEnter Right Choice......\n");
	}break;
	}
	return c;
}
// Function for taking details of passengers
int details(int k)
{
	struct Rec *ptr;
	int i,a;
	ptr = (struct Rec*) malloc(k *sizeof(struct Rec));
	for (i = 0; i < k; i++) {
		printf("Enter The %dth Passenger Name: ", i+1);
		fflush(stdin);
		scanf("%s",&(ptr)->name[i]);
		printf("Enter The %dth Passenger Gender: ", i+1);
		fflush(stdin);
		scanf("%s",&(ptr)->gen[i]);
		printf("Enter The %dth Passenger Age: ", i+1);
		fflush(stdin);
		scanf("%d",&(ptr)->Age);
		printf("Passenger %d details---->\n",i+1);
		printf("%s\n%s\n%d\n",(ptr)->name,(ptr)->gen,(ptr)->Age);
	}
    return 0;
}
// Function for chosing seats
int seat(int p)
{
	int i;
	printf("\t		 -:SEAT MATRIX:-	 \n");
	printf("\t(U) (M)	 (L) (L)  (U)\n\n");
	printf("\t01 02	 03\t04	 05\n\n");
	printf("\t06 07	 08\t09	 10\n");
	printf("\t11 12	 13\t14	 15\n\n");
	printf("\t16 17	 18\t19	 20\n");
	printf("\t21 22	 23\t24	 25\n\n");
	printf("\t26 27	 28\t29	 30\n");
	printf("\t31 32	 33\t34	 35\n\n");
	printf("\t36 37	 38\t39	 40\n");
	printf("\t41 42	 43\t44	 45\n\n");
	printf("\t46 47	 48\t49	 50\n");
	printf("\t51 52	 53\t54	 55\n\n");
	printf("\t56 57	 58\t59	 60\n");
	printf("\n");
	printf("\n");
	printf("\tEnter Seat Number(s)----> ");
	for (i = 0; i < p; i++){
		scanf("%d", &a[i]);
    }
    return 0;
}
// Function for printing receipt
int bill(int y, int j)
{
	int i;
	printf("\n");
	printf("\n");
	printf("\t\tSource Place: Chennai \n");
	printf("\t\tDestination Place: ");
	puts(des);
	printf("\t\tBoarding Station: ");
	puts(station);
	printf("\t\tTrain Is: ");
	puts(train);
	printf("\t\tAllocated Class: ");
	puts(cla);
	printf("\t\tBoarding Time: %d:0%d\n", time1, time2);
	printf("\t\tTotal Bill Amount: %d\n", y);
	printf("\t\tAllocated Seat(s) is/are: ");
	for (i = 0; i < j; i++) {
		printf(" %d ", a[i]);
	}
	printf("\n");
	printf("\n");
	printf("\n");
	printf("\t\t----------------------------------------------\n");	
	printf("\t\t                  Thank You!                  \n");
	printf("\t\t----------------------------------------------\n");	

    return 0;
}
