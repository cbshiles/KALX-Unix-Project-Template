PROJ = $(notdir $(shell pwd))
HDRS = $(wildcard *.h)
SRCS = $(wildcard *.cpp)
OBJS = $(SRCS:.cpp=.o)

CXXFLAGS += -Wall -std=c++11 -I$(ROOT)/include
LDFLAGS += -L$(ROOT)/lib

all:: $(PROJ)
	./$(PROJ)

$(PROJ):: $(OBJS)
	$(CXX) $(CXXFLAGS) $^ -o $@

.PHONY: clean
clean:
	-rm -f $(PROJ) *.exe *.o *.obj

.PHONY: depends
depends:
	@cc -MM $(CXXFLAGS) $(SRCS) | tail +1 \
	| sed -e 's;c:;/c;' -e 's;'$(ROOT)';\$$\(ROOT\);g'

# :r!depends
hello.o: hello.cpp
