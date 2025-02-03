# Details-of-a-person4

// Online C compiler to run C program online
#include <stdio.h>
#include <string.h>
struct person{
    char name[50];
    int age;
    char city[50];
};
int main(){
    struct person people[5]={
        {"Shiva",25,"India"},
        {"Ram",18,"America"},
        {"Lakshman",15,"New York"},
        {"Rishi",35,"Italy "},
        {"Megha",28,"Paris"}
    };
    char searchname[50];
    int i,found=0;
    printf("Enter the name to search:");
    scanf("%[^\n]",searchname);
    for(i=0;i<5;i++){
        if(strcmp(people[i].name,searchname)==0) {
            printf("\nDetails of %s: \n", people[i].name);
            printf("Age: %d\n", people[i].age);
            printf("City: %s\n", people[i].city);
            found=1;
            break;
        }
    }
    if(!found){
        printf("\nPerson with name '%s' not found in the list.\n",searchname);
    }
    return 0;
    }
