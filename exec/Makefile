# **************************************************************************** #
#                                                           LE - /             #
#                                                               /              #
#    Makefile                                         .::    .:/ .      .::    #
#                                                  +:+:+   +:    +:  +:+:+     #
#    By: kcabus <kcabus@student.le-101.fr>          +:+   +:    +:    +:+      #
#                                                  #+#   #+    #+    #+#       #
#    Created: 2018/04/06 14:53:11 by kcabus       #+#   ##    ##    #+#        #
#    Updated: 2018/12/03 09:39:39 by bpajot      ###    #+. /#+    ###.fr      #
#                                                          /                   #
#                                                         /                    #
# **************************************************************************** #

.PHONY: all clean fclean re

NAME = libexec.a

WFLAGS = -Wall -Wextra -Werror -g

SRC_PATH = ./srcs/
INC_PATH = ./includes/
OBJ_PATH = ./obj/
LIB_PATH = ../libft/


SRC = $(addprefix $(SRC_PATH),$(N_SRCS))
OBJ = $(addprefix $(OBJ_PATH),$(OBJ_NAME))
INC = -I $(INC_PATH) -I $(LIB_PATH)

OBJ_NAME = $(N_SRCS:.c=.o)

N_SRCS =	and_or.c					\
			cd.c						\
			cd_suite.c					\
			check_bin.c					\
			check_builtin.c				\
			check_builtin2.c			\
			delete_heredoc.c			\
			echo.c						\
			env.c						\
			equal.c						\
			execve.c					\
			exit.c						\
			export.c					\
			fork.c						\
			ft_delete_history.c			\
			ft_dollar.c					\
			ft_err_hist.c				\
			ft_history.c				\
			ft_history_struct.c			\
			ft_history_struct_suite.c	\
			ft_history_suite.c			\
			ft_history_suite2.c			\
			ft_len_tab.c				\
			ft_redir_in.c				\
			ft_redir_out.c				\
			ft_save_p_env.c				\
			ft_tilde_dollar.c			\
			getenv.c					\
			infos_hist.c				\
			manage_redir.c				\
			manage_signal.c				\
			pipes.c						\
			redir.c						\
			ret_display.c				\
			setenv.c					\
			set.c						\
			unset.c						\
			unsetenv.c

all : $(NAME)

$(NAME):	$(OBJ)
			@ar rc $(NAME) $(OBJ) 
			@printf "\033[35;5m exec OK ! \n\033[0m"

$(OBJ_PATH)%.o:	$(SRC_PATH)%.c
				@mkdir -p $(OBJ_PATH)
				@gcc -c $(WFLAGS) $(INC) -o $@ $<
				@printf "\033[45m \033[0m"
	
clean :
		@rm -rf $(OBJ_PATH)

fclean : 	clean
			@rm -rf $(NAME)

re : fclean clean all
