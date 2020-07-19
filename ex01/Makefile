# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gekang <gekang@student.42seoul.kr>         +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/07/15 09:30:41 by gekang            #+#    #+#              #
#    Updated: 2020/07/19 22:11:54 by gekang           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #


CFILES	= srcs/ft_putchar.c srcs/ft_putstr.c srcs/ft_strlen.c srcs/ft_strcmp.c srcs/ft_swap.c #no need for ./ (it starts from cwd)
OFILES	= ${CFILES:.c=.o}
INCL	= includes
TARGET	= libft.a
CREATELIB	= ar rcs
CC		= gcc
REMOVE		= rm -f
CFLAGS	= -Wall -Wextra -Werror

.c.o:
	${CC} ${CFLAGS} -c $< -o ${<:.c=.o} -I${INCL}

${TARGET}: ${OFILES}
	${CREATELIB} ${TARGET} ${OFILES}

all: ${TARGET}

clean:
	${REMOVE} ${OFILES}

fclean: clean
	${REMOVE} ${TARGET}

re: fclean all

norm :
	norminette -R CheckForbiddenSourceHeader */*.[ch]

.PHONY: all clean fclean re .c.o norm
