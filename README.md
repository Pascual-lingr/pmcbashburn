README of PMC-BashBurn:
=======================
PMC-BashBurn is released under the GNU GPL v2

This is a custom distribution of BashBurn 2.0
including some Linux-cdgrab functionalities.
Stable version (09-08-2017).

Pascual Martínez Cruz --> pascual89@hotmail.com

CONSTRUCTION
============

PMC-BashBurn 2.0 are delevoped from original BashBurn 2.0 sources.

List of Modifications:

./burning/burning.sh --> # PMC ; Support to burn .ext2 images on CD or DVD (image is burned with cdrecord); #PMC-ext2-ini #PMC-ext2-end
			 # PMC ; Changed growisofs call to burn iso images on DVD. #PMC-dvdburn-ini #PMC-dvdburn-end

./config/reset_options.sh --> # PMC; Small Changes. #PMC-C-ini #PMC-C-end (CD label).

./func/ext2func.sh --> Implements API to support ext2 file system. New func file.
			    # PMC-ini PMC-end
			    # This file contains functionality for ext2 file handling
			    # Adapted from original file isofunc.sh
			    # Code ported from Linux-cdgrab 0.5 Beta.
			    
./func/DVDblankfunc.sh --> Implemens API to DVD+-RW format. New func file.
			    # ./func/DVDblankfunc.sh --> Pascual Martinez Cruz
			    # Format support to DVD+RW and DVD-RW disks
			    # in PMC-BashBurn 2.0
			    # Ported from Linux-cdgrab 0.5 beta
			    # Adapted from original file ext2func.sh

./func/isofunc.sh --> # Some Changes to PMCBashBurn 2.0 ; PMC-ini PMC-end
			    # Changed iso file generated: ${BBBURNDIR}/PMC-BashBurn.iso

./lang --> Only English and Spanish languajes are used.
	   Rest languajes are not maintained in this release.

./lang/English/BashBurn.lang --> # PMC ; Modifications in messages

./lang/English/check_path.lang --> # PMC ; Modifications in messages

./lang/English/DVDblank_menu.lang --> # PMC ; English languaje for DVD Blanking Menu. New lang file.

./lang/English/ext2_menu.lang --> # PMC ; English languaje for Ext2 Menu. New lang file.

./lang/English/PMCBashBurn.lang --> # PMC ; BashBurn.lang modified file.

./lang/English/BashBurn.lang --> # PMC ; BashBurn.lang modified file.

./lang/Spanish/BashBurn.lang --> # PMC ; BashBurn.lang modified file.

./lang/Spanish/PMCBashBurn.lang --> # PMC ; BashBurn.lang modified file.

./lang/Spanish/check_path.lang --> # PMC ; Modifications in messages

./lang/Spanish/configure.lang --> # PMC ; Modifications in messages

./lang/Spanish/datadefine.lang --> # PMC ; Modifications in messages

./lang/Spanish/DVDblank_menu.lang --> # PMC ; Spanish languaje for DVD Blanking Menu. New lang file.

./lang/Spanish/ext2_menu.lang --> # PMC ; Spanish languaje for Ext2 Menu. New lang file.

./menus/ext2_menu.sh --> # PMC ; Adapted iso_menu.sh menu program, to ext2 file system menu. New Menu file.

./menus/DVDblank_menu.sh --> # PMC ; Adapted ext2_menu.sh menu program.
			     #       Add support to format DVD+RW and DVD-RW
			     #       in PMC-BashBurn. New Menu file.

./misc/colors.idx --> # PMC; Modified UI colors, code from Linux-cdgrab 0.5 Beta.

./misc/commands.idx --> # PMC; Support for dd and mke2fs formatter. #PMC-dd-ini #PMC-dd-end
			# PMC; Support for DVD Blanking. #PMC-dvdblanking-ini #PMC-dvdblanking-end

./misc/loopback.sh --> # PMC; Support for ext2 images. #PMC-ext2-ini #PMC-ext2-end

./misc/oldpmcbashburncolors.idx --> # PMC; original colors.idx file used in PMC-Bashburn. Additional file.
				    # To use this color UI file rename it to colors.idx
				    # Make a backup copy of original color.idx file before rename this file.
				    
./ChangeLog # PMC; Some text added.

./credits # PMC; Some text added.

./CREDITS # PMC; Some text added.

./Install.sh --> # PMC; Change directory and command names to generate an installation independent of BashBurn.
		 # Changed some display messages
		 
./howto and HOWTO --> PMC; Edited text.

./credits and CREDITS --> PMC; Edited text.

./ChangeLog --> PMC; Edited text.

./README.PMC --> PMC; New readme .txt file for this release.

Thanks for use PMC-BashBurn.
