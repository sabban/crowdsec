ifeq ($(OS), Windows_NT)
	SHELL := pwsh.exe
	.SHELLFLAGS := -NoProfile -Command
	EXT = .exe
endif

PLUGIN=slack
BINARY_NAME = notification-$(PLUGIN)$(EXT)

GOCMD = go
GOBUILD = $(GOCMD) build

build: clean
	$(GOBUILD) $(LD_OPTS) $(BUILD_VENDOR_FLAGS) -o $(BINARY_NAME)

.PHONY: clean
clean:
	@$(RM) $(BINARY_NAME) $(WIN_IGNORE_ERR)
