# workspace (all)

###########################################################

ifeq (,$(PLATFORM))
PLATFORM=$(UNION_PLATFORM)
endif

ifeq (,$(PLATFORM))
$(error please specify PLATFORM, eg. PLATFORM=trimui make)
endif

###########################################################

.PHONY: all

all:
	cd ./$(PLATFORM)/libmsettings && make
	cd ./$(PLATFORM) && make early # eg. other libs
	cd ./$(PLATFORM)/keymon && make
	cd ./all/minui/ && make
	cd ./all/minarch/ && make
	cd ./all/battery/ && make
	cd ./all/clock/ && make
	cd ./all/libbatmondb/ && make
	cd ./all/batmon/ && make
	cd ./all/libgametimedb/ && make
	cd ./all/gametime/ && make
	cd ./all/gametimectl/ && make
	cd ./all/syncsettings/ && make
	cd ./all/nextval/ && make
	cd ./all/settings/ && make
	cd ./all/ledcontrol/ && make
	cd ./all/bootlogo/ && make
# BUILDOPTION: don't forget to uncomment this to rebuild cores from  source, idk if this was left commented by mistake, but I actually agree on leaving this commented out by default as they take a long while to build and only really need building if someone bothered to pull the repo's manually and there are actually updates to any core worth including in new MinUI Next releases.
	# cd ./$(PLATFORM)/cores && make
	cd ./$(PLATFORM) && make

clean:
	cd ./$(PLATFORM)/libmsettings && make clean
	cd ./$(PLATFORM)/keymon && make clean
	cd ./all/minui/ && make clean
	cd ./all/minarch/ && make clean
	cd ./all/battery/ && make clean
	cd ./all/clock/ && make clean
	cd ./all/libbatmondb/ && make clean
	cd ./all/batmon/ && make clean
	cd ./all/libgametimedb/ && make clean
	cd ./all/gametimectl/ && make clean
	cd ./all/gametime/ && make clean
	cd ./all/minput/ && make clean
	cd ./all/syncsettings/ && make clean
	cd ./all/nextval/ && make clean
	cd ./all/settings/ && make
	cd ./all/ledcontrol/ && make
	cd ./all/bootlogo/ && make
	cd ./all/scraper/ && make
	cd ./$(PLATFORM) && make clean