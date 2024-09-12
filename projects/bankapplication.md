---
layout: project
type: project
image: img/database_1.jpg
title: "Bank Database Application"
date: 2015
published: true
labels:
  - C
  - Database
  - User Interface
summary: "Bank database application developed for ICS 212 class in C langugage. Provides user interface to interact with a bank database using a record structure."
---

This project is a bank database management system developed in C during my semester in ICS 212. Designed to handle user records with functionalities for adding, finding, deleting, and printing account records. The program uses a linked list to manage bank records and provides a command-line interface for users to interact with the database. Features include reading and writing data to a file, ensuring persistent storage, and implementing memory management to prevent leaks.

Snippet of the user interface code, highlighting the functionalities present in the application :

```c
void user_interface(struct record **start)
{

    char input[150];
    char name[25];
    char address[100];
    int accountno;

    printf("Welcome to the Bank Database Application\n");

    while (1)
    {
        printf("\nPlease choose an action to perform (type 'quit' to exit):\n");
        printf("add: Add a new record in the database\n");
        printf("printall: Print all records in the database\n");
        printf("find: Find record(s) with a specified account number\n");
        printf("delete: Delete exist record(s) from the database using the account number as a key \n");
        printf("quit: Quit the program\n");
        printf("> ");
        scanf("%s", input);
        while (getchar() != '\n');

        if (strncmp(input, "add", strlen(input)) == 0 && strlen(input) <= strlen("add"))
        {
            printf("Enter account number: ");
            scanf("%d", &accountno);
            while (getchar() != '\n');

            printf("Enter name: ");
            fgets(name, sizeof(name), stdin);
            name[strcspn(name, "\n")] = 0;

            printf("Enter address, followed by an empty line to finish:\n");
            getaddress(address, sizeof(address));

            if (addRecord(start, accountno, name, address) == -1)
            {
                printf("Failed to add record. Duplicate account number.\n");
            }
            else
            {
                printf("Record added successfully.\n");
            }
        }
        else if (strncmp(input, "printall", strlen(input)) == 0 && strlen(input) <= strlen("printall"))
        {
            printAllRecords(*start);
        }
        else if (strncmp(input, "find", strlen(input)) == 0 && strlen(input) <= strlen("find"))
        {
            int accountNumFind;
            printf("Enter account number to find: ");
            scanf("%d", &accountNumFind);
            while (getchar() != '\n');

            if (findRecord(*start, accountNumFind) == -1)
            {
                printf("No record found with account number: %d\n", accountNumFind);
            }
        }
        else if (strncmp(input, "delete", strlen(input)) == 0 && strlen(input) <= strlen("delete"))
        {
            int accountNumDelete;
            printf("Enter account number to delete: ");
            scanf("%d", &accountNumDelete);
            while (getchar() != '\n');

            if (deleteRecord(start, accountNumDelete) == -1)
            {
                printf("No record found with account number: %d\n", accountNumDelete);
            }
            else
            {
                printf("Record with account number %d deleted.\n", accountNumDelete);
            }
        }
        else if (strncmp(input, "quit", strlen(input)) == 0 && strlen(input) <= strlen("quit"))
        {
            printf("Saving records and exiting program.\n");

            if (writefile(*start, "records.txt") == -1)
            {
                printf("Failed to save records to file.\n");
            }

            return;
        }
        else
        {
            printf("Invalid option. Please try again.\n");
        }
    }
}
