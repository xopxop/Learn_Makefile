CXX			:= g++
CXXFLAGS	:= -Wall -Wuninitialized -std=c++17 -g
LDFLAGS		:= -L/usr/lib -Llib
BUILD		:= ./build
OBJ_DIR		:= $(BUILD)/objects
INCLUDE		:= -Iinclude/
SRC			:=						\
	$(wildcard src./*.cpp)			\
	$(wildcard src/modules/*.cpp)	\

OBJECTS		:= $(SRC:%.cpp=$(OBJ_DIR)/%.o)

all: mkdirs $(BUILD)/program

$(OBJ_DIR)/%.o: %.cpp
	$(CXX) $(CXXFLAGS) $(INCLUDE) -c $< -o $@

$(BUILD)/program: $(OBJECTS)
	$(CXX) $(CXXFLAGS) -o $(APP_DIR)/$(TARGET) $^ $(LDFLAGS)

.PHONY: all mkdirs clean

mkdirs:
	mkdir -p $(OBJ_DIR)

clean:
	rm -rvf $(BUILD)/*