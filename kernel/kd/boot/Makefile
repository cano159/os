################################################################################
#
#   Copyright (c) 2014 Minoca Corp.
#
#    This file is licensed under the terms of the GNU General Public License
#    version 3. Alternative licensing terms are available. Contact
#    info@minocacorp.com for details. See the LICENSE file at the root of this
#    project for complete licensing information.
#
#   Binary Name:
#
#       Kernel Debugger (Boot)
#
#   Abstract:
#
#       This library builds a portion of the Kernel Debugger Library for use in
#       the boot environment.
#
#   Author:
#
#       Chris Stevens 18-Mar-2014
#
#   Environment:
#
#       Boot
#
################################################################################

BINARY = kdboot.a

BINARYTYPE = library

INCLUDES += $(SRCDIR)/..;

VPATH += $(SRCDIR)/..:

OBJS = kdebug.o   \

ARMV7_OBJS = armv7/kdarch.o        \
             armv7/kdsup.o         \
             armv7/kdsupc.o        \
             boot/armv7/kdatomic.o \

ARMV6_OBJS = $(ARMV7_OBJS)

X86_OBJS = x86/kdarch.o   \
           x86/kdsup.o    \

EXTRA_SRC_DIRS = x86 armv7 armv6 boot/armv7

include $(SRCROOT)/os/minoca.mk

