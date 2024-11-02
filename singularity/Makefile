AUTHOR=Radu Daia <radu.daia@pm.me>
VERSION=v1.0.0

BUILDER=apptainer
BUILD_FLAGS=--fakeroot --force
SRC = ubuntu-yocto.def
TARGET = ubuntu-yocto.sif
BUILD_DIR=./build

all: $(TARGET)

setup:
	mkdir -p $(BUILD_DIR)

$(TARGET): $(SRC) setup
	$(BUILDER) build $(BUILD_FLAGS) $(BUILD_DIR)/$@ $<

.PHONY: clean
clean:
	rm -rf $(BUILD_DIR)


