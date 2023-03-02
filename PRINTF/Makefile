NAME		= libftprintf.a

SRCS		= ft_printf.c \
			  ft_printhex.c \
			  ft_printptr.c \
			  ft_unsignedprint.c\
			  ft_printf_utils.c \
			  
				
OBJS		= $(SRCS:%.c=%.o)

FLAGS		= -Wall -Werror -Wextra

LIBFTPATH	= ./libft

LIBFT		= libft.a

CC			= gcc $(FLAGS)

.o:.c
	$(CC) $(OBJS) $< $(LIBFTPATH)/$(LIBFT) -o $(<:.c=.o)

all: $(NAME)

$(NAME): $(LIBFT) $(OBJS)
	cp $(LIBFTPATH)/$(LIBFT) $(NAME)
	ar rc $(NAME) $(OBJS)
	ranlib $(NAME)

$(LIBFT):
	make -C $(LIBFTPATH) all

clean:
	rm -f $(OBJS)
	make -C $(LIBFTPATH) clean

fclean: clean
	rm -f $(NAME)
	make -C $(LIBFTPATH) fclean

re: fclean all