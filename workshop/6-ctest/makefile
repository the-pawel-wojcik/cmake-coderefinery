.PHONY: all config build clean

all: clean config build test

config:
	cmake -S src -B build
	mv build/compile_commands.json src/

build:
	cmake --build build

test:
	ctest --test-dir build

clean:
	-rm -frv build
