# Makefile for stklos-gtk-base example 
#
#          Author: Erick Gallesio [eg@essi.fr]
#   Creation date:  8-Apr-2008 18:28 (eg)
#Last file update:  9-Apr-2008 16:03 (eg)

CC     = gcc
CFLAGS = -Wall			 	\
	-DG_DISABLE_DEPRECATED 	 	\
	-DGDK_DISABLE_DEPRECATED 	\
	-DGDK_PIXBUF_DISABLE_DEPRECATED \
	-DGTK_DISABLE_DEPRECATED


all: simple simple-in-C

simple: simple.stk
	stklos-compile -o simple simple.stk


simple-in-C: simple-in-C.c 
	$(CC) simple-in-C.c -o simple-in-C $(CFLAGS) \
              `pkg-config gtk+-2.0 --cflags --libs`

clean:
	/bin/rm -f *~ simple simple-in-C

