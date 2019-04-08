
# CC := $(CROSS_COMPILE)gcc
# CC := /local/mnt/workspace/leiwan/code/hana-12-26/poky/build/tmp-glibc/work/x86_64-linux/gcc-cross-aarch64/7.3.0-r0/recipe-sysroot-native/usr/bin/aarch64-agl-linux-gcc
CC := /local/mnt/workspace/leiwan/bin/gcc-linaro-5.3-2016.02-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc
# CC := aarch64-linux-gnu-gcc

INCLUDEDIR := -I../../../drivers/staging/android/uapi/
# INCLUDEDIR += -I../../../include/uapi/linux/

CCFLAGS := $(INCLUDEDIR) -Wall -O2 -g

all: ionapp_export ionapp_import

ionapp_import : ionapp_import.c
	$(CC) -o ionapp_import.out ionapp_import.c ipcsocket.c ionutils.c $(CCFLAGS)

ionapp_export : ionapp_export.c
	$(CC) -o ionapp_export.out ionapp_export.c ipcsocket.c ionutils.c $(CCFLAGS)

clean:
	rm -rf *.o *~ *.out
