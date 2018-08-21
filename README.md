#include <stdio.h>
#include <string.h>

int main(void)
{
  char str[3];
  printf("Enter two characters: ");
  if(!fgets(str, sizeof(str), stdin))
    return 1;

  if(str[0] == '\n' || str[1] == '\n') {
    printf("Not enough characters\n");
  } else {
    if(str[0] >= 'a' && str[0] <= 'z')
      printf("First char is lowercase\n");
    else
      printf("First char is not lowercase\n");

    if(str[0] >= '0' && str[0] <= '9')
      printf("First char is a digit\n");
    else
      printf("First char is not a digit\n");

    if(str[0] == str[1])
      printf("First and second chars are the same\n");
    else
      printf("First and second chars are not the same\n");
  }

  return 0;
}
