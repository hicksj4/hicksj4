---
layout: project
type: project
image: img/database_1.jpg
title: "Bank Database Application"
date: 2017
published: true
labels:
  - C
  - Database
  - User Interface
summary: "Bank database application developed for ICS 212 class in C langugage. Provides user interface to interact with a bank database using a record structure."
---

This project involved the development of a command-line-based bank database management system written in C. The application was designed to handle user records, allowing users to add, find, delete, and print account records in a linked list structure. The main challenge was implementing efficient data management while maintaining the integrity and performance of the system, especially when interacting with a growing database of records. Key features included reading and writing data to a file to ensure persistent storage, managing user inputs through a command-line interface, and implementing dynamic memory management to prevent leaks. This project provided an opportunity to explore real-world applications of data structures, file I/O, and command-line interaction in software development.

My role in this project was to code the core logic and implementation of the bank database system independently. I was responsible for writing the functions that managed the linked list of records, such as adding, finding, and deleting records, as well as reading from and writing to a file. I also interacted with the command line extensively to test and refine the application's performance, ensuring all features worked as intended. While the professor provided a general structure and guidelines for the project, I took full control of the implementation, focusing on problem-solving and debugging as I built the application from the ground up.

This project was a valuable learning experience in understanding the intricacies of memory management in C, particularly the critical importance of properly managing dynamic memory allocation and deallocation. I gained hands-on experience with pointers, which are more abstracted away in languages like Java and C#, highlighting how direct manipulation of memory can impact application stability and performance. Working with C also taught me to pay closer attention to error handling, debugging, and efficient code practices to prevent issues such as memory leaks and segmentation faults. Overall, the project deepened my appreciation for low-level programming and the careful attention required when working closely with system resources.

Snippet of the user interface code, highlighting the functionalities present in the application :

<pre><code class="language-c">

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

</code></pre>
