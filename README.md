# Get Next Line

The project aims to create a function that returns the first line of a file.

See the [subject](./subject.pdf) for more information.

## Table of Contents (TOC)

- [What's in it?](#whats-in-it)
  - [Mandatory](#mandatory)
  - [Bonus](#bonus)
- [Requirements](#requirements)
- [How to use it?](#how-to-use-it)
- [How to create a Main for Get Next Line](#how-to-create-a-main-for-get-next-line)
- [License](#lisence)

## What's in it?

### Mandatory

> In the mandatory part, you only have the simple version of the get_next_line function, which allows you to handle only one file.

### Bonus

> The difference between the bonus and the mandatory is that in the bonus, you can handle multiple files at the same time with the same get_next_line function.

## Requirements

> To run this functio you need a C compiler and the standard C libraries.

## How to use it?

1. Clone the repository.

```shell
git clone git@github.com:Diogo13Antunes/42Cursus_Get_Next_Line.git
```

2. Go to the repository.

```shell
cd 42Cursus_Get_Next_Line
```

3. Choose the version you whant ( Mandatory / Bonus ).

```shell
cd Mandatory
```

```shell
cd Bonus
```

4. Compile the correct Version

```shell
gcc main_example.c get_next_line.c get_next_line_utils.c
```

```shell
gcc main_bonus_example.c get_next_line_bonus.c get_next_line_utils_bonus.c
```

6. Cleaning

```shell
rm -rf a.out
```

## How to create a Main for Get Next Line

> To use this function you need to create a main like this.

    #include "get_next_line.h"
    #include "get_next_line_bonus.h"
    #include <fcntl.h>

    int main(void)
    {
        int     fd = -1;
        char    *line;
    
        fd = open([FILENAME], O_RDONLY);
        line = get_next_line(fd);
        printf("%s", line);
        free(line);
        close (fd);
    }

> Do not forget to close the file descriptor (fd) and free the dynamically allocated returned line.

## Lisence

Check all the terms [here](/LICENSE).
