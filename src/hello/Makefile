NAME = $(shell pwd)
HDRS = $(wildcard *.h)
SRCS = $(wildcard *.cpp)
OBJS = $(SRCS:.cpp=.o)

all: $(OBJS)	
	./$(NAME)
	
$(NAME): $(OBJS)
	$(CXX) $(CXXFLAGS) $^ -o $@
.PHONY: depends
