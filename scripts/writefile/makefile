#Makefile for load
#auther: Jason Hu
#time: 2020/1/26

DD = dd

FILE = ./shadow.nes

FILE_OFF = 0
FILE_CNTS = 100

#img dir
IMG_DIR = ../../developments/image/

DISK_IMG = d.img
DISK_VHD = d.vhd
DISK_VMDK = d-flat.vmdk

HD_IMG = $(IMG_DIR)$(DISK_IMG)
HD_VHD = $(IMG_DIR)$(DISK_VHD)
HD_VMDK = $(IMG_DIR)$(DISK_VMDK)

#First read here
.PHONY: all

all: img vhd vmdk

img:
	$(DD) if=$(FILE) of=$(HD_IMG) bs=512 seek=$(FILE_OFF) count=$(FILE_CNTS) conv=notrunc
	
vhd:
	$(DD) if=$(FILE) of=$(HD_VHD) bs=512 seek=$(FILE_OFF) count=$(FILE_CNTS) conv=notrunc
	
vmdk:
	$(DD) if=$(FILE) of=$(HD_VMDK) bs=512 seek=$(FILE_OFF) count=$(FILE_CNTS) conv=notrunc
