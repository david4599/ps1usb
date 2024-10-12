include ../config/Makefile.conf

TARGET = ps1usb_example

SRCS = example.c libsn_usb.c
CFLAGS = -O2

include $(PSXDIR)/common.mk


all:
	mkpsxiso -y -q ps1usb_example.xml
	../ps1transfer/ps1transfer -e -f ps1usb_example.ps-exe -c -p .

clean:
	rm -f $(OBJS) $(BINDIR)Overlay.* $(BINDIR)*.elf $(BINDIR)*.ps-exe $(BINDIR)*.map $(BINDIR)$(TARGET).bin $(BINDIR)$(TARGET).cue $(DEPS)


.PHONY: all clean

