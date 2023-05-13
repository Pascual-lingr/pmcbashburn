README of PMC-BashBurn:
=======================
PMC-BashBurn is released under the GNU GPL v2

This is a custom distribution of BashBurn 2.0 including some Linux-cdgrab functionalities.
Based from original BashBurn 2.0 release made by Anders Linden.
Uploaded to 2.1 ; Stable (26-03-2023).

Pascual Martínez Cruz --> pascual89@hotmail.com

CONSTRUCTION
============

PMC-BashBurn 2.1 are developed from original BashBurn 2.0 sources.

List of Modifications v2.1:

./CDMixed_menu.sh --> Support for Mixed CD, New menu file.
		      Call burning.sh with new --mixcd option
		      execute new cdmixto burning function.

./func/bincuefunc.sh --> Support to generate bin/cue files from CD on unit burner 
			 # From linux-cdgrab 0.5 r2 # PMC-INI # PMC-END

./menus/BinCue_menu.sh --> Support to generate bin/cue files from CD.			 
			   New menu file. Pascual Martínez Cruz
			   Interface for manage the burn or generation of bin/cue files.

./lang/English/bincue.lang --> Impact of BinCue_menu, English messages for menu.
./lang/Spanish/bincue.lang --> Impact of BinCue_menu, Spanish messages for menu.

./burning/burning.sh --> Support to burn DVD Video (DVD-9).
			 dvd_video function implemented, from Linux-cdgrab-0.5 r2.
			 Burns DVD-9 Video from harddisk files into DVD (DVD-R/+R/-RW/+RW)
                         Support to burn Mixed CD, from linux-cdgrab-0.5r2
			 Mixed CD (Data tracks + Audio Tracks).
			 Capture error if no .iso files found in /tmp/burn burning iso image.

./lang/English/burning.lang --> Added languaje to dvd_video, from Linux-cdgrab-0.5 r2.
./lang/Spanish/burning.lang --> Added languaje to dvd_video, from Linux-cdgrab-0.5 r2.

./lang/English/PMCBashBurn.lang --> Option DVD-Video added, credits.
./lang/Spanish/PMCBashBurn.lang --> Option DVD-Video added, credits.

./menus/DVDVideo_menu.sh --> New menu file.
			     Call burning.sh with new --dvdvideo option
			     execute new dvd_video burning function.

./PMCBashBurn.sh --> - Fix error of infinity loop in force_quit function,
		     break command not works and program can execute a
		     infinity loop, needs kill process to exit application.

		     - Implemented new option to burn Mixed CD (Data + Audio Tracks)

		     - Implemented new option to burn DVD-9 Video from hardrive files
		     in DVD+R/RW and DVD-R/RW
		     
		     - Calls new bin/cue submenu.

./func/isofunc.sh --> Extract iso-9660 img file from DVD; # From linux-cdgrab 0.5r2 #PMC-ini #PMC-end
./lang/English/iso_menu.lang --> Impact of extraer_isoDVD_dd function # From linux-cdgrab 0.5r2
./lang/Spanish/iso_menu.lang --> Impact of extraer_isoDVD_dd function # From linux-cdgrab 0.5r2
./menus/iso_menu.sh --> New option to extrac iso-9660 image file from DVD data disk.

./lang/English/commonfunctions.lang --> Impact of text_una_sola_grabadora function # From linux-cdgrab 0.5r2
./lang/Spanish/commonfunctions.lang --> Impact of text_una_sola_grabadora function # From linux-cdgrab 0.5r2
./misc/commonfunction.sh --> Implemented text_una_sola_grabadora function # From linux-cdgrab 0.5r2 # PMC-ini #PMC-end

./menu/data_menu --> New option to copy data DVD. Implemented copy_data_dvd function; Copy DVD to DVD.
./burning/burning.sh --> Implemented --dirdvdimage burning calling to execute growisofs directly. Function direct_dvd_image_burn

./Install.sh --> Create hardlink of PMCBashBurn.sh, other fixes.
./misc/check_path.sh --> Shows comands of the new functionalities.

./howto --> Explanation of new options.
./HOWTO --> Explanation of new options.
./Changelog --> Changelog application file
./README.PMC --> Of course, this file.

Added erase_pmcbb.sh file, to erase a PMCBashBurn instalation.

List of Modifications (v2.0 first release):

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

./TODO --> PMC; Not maintained file in PMC-BashBurn
./todo --> PMC; Not maintained file in PMC-BashBurn

./README.PMC --> PMC; New readme .txt file for this release.

Thanks for use PMC-BashBurn.
