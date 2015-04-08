kernel_mkboot_tools
===============

### Unpack and repack boot.img,support dtb(dt.img):
	linhphi@KmaSecurity:~/Android/mkbootimg$ ./mkboot boot.img boot
	Unpack & decompress boot.img to boot
  	kernel         : zImage
  	ramdisk        : ramdisk
  	page size      : 2048
 	kernel size    : 5150776
  	ramdisk size   : 815683
 	dtb size       : 561152
 	base           : 0x00000000
 	kernel offset  : 0x00008000
 	ramdisk offset : 0x05000000
 	tags offset    : 0x04800000
 	dtb img        : dt.img
  	cmd line       : console=ttyHSL0,115200,n8 androidboot.hardware=g2 user_debug=31 msm_rtb.filter=0x0
	ramdisk is gzip format.
	Unpack completed.


	linhphi@KmaSecurity:~/Android/mkbootimg$ ./mkboot boot.img boot
	Unpack & decompress boot.img to boot
  	kernel         : zImage
  	ramdisk        : ramdisk
  	page size      : 2048
  	kernel size    : 5150776
  	ramdisk size   : 815683
  	dtb size       : 561152
  	base           : 0x00000000
  	kernel offset  : 0x00008000
  	ramdisk offset : 0x05000000
  	tags offset    : 0x04800000
  	dtb img        : dt.img
  	cmd line       : console=ttyHSL0,115200,n8 androidboot.hardware=g2 user_debug=31 msm_rtb.filter=0x0
	ramdisk is gzip format.
	Unpack completed.


### Create a dt.img:
		linhphi@KmaSecurity:/media/diskd/kernel/LG-f320l_JB_Opensource/Kernel$ scripts/dtbTool -s 2048 -o arch/arm/boot/dt.img -p scripts/dtc/ arch/arm/boot/
		DTB combiner:
		  Input directory: '/media/diskd/kernel/LG-f320l_JB_Opensource/Kernel/arch/arm/boot/'
		  Output file: '/media/diskd/kernel/LG-f320l_JB_Opensource/Kernel/arch/arm/boot/dt.img'
		Found file: msm8974-sec-ks01-r03.dtb ... chipset: 2114015745, platform: 3, rev: 0
		Found file: msm8974-sec-ks01-r07.dtb ... chipset: 2114015745, platform: 7, rev: 0
		Found file: msm8974-sec-ks01-r06.dtb ... chipset: 2114015745, platform: 6, rev: 0
		Found file: msm8974-sec-ks01-r04.dtb ... chipset: 2114015745, platform: 4, rev: 0
		Found file: msm8974-sec-ks01-r11.dtb ... chipset: 2114015745, platform: 11, rev: 0
		Found file: msm8974-sec-ks01-r02.dtb ... chipset: 2114015745, platform: 2, rev: 0
		Found file: msm8974-sec-ks01-r00.dtb ... chipset: 2114015745, platform: 0, rev: 0
		Found file: msm8974-sec-ks01-r05.dtb ... chipset: 2114015745, platform: 5, rev: 0
		Found file: msm8974-sec-ks01-r01.dtb ... chipset: 2114015745, platform: 1, rev: 0
		=> Found 9 unique DTB(s)

		Generating master DTB... completed


### dtbToolCM support dt-tag & dtb v2(https://github.com/CyanogenMod/android_device_qcom_common/tree/cm-11.0/dtbtool):

 	dtbToolCM -s 2048 -d "htc,project-id = <" -o arch/arm/boot/dt.img -p scripts/dtc/ arch/arm/boot/

