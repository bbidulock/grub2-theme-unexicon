
ACLOCAL_AMFLAGS = -I m4

SUBDIRS =

ChangeLog:
	( \
	  echo -e "# created with git log --stat=76 -M -C|fmt -sct -w80\n" ; \
	  git log --stat=76 -M -C|fmt -sct -w80 ; \
	)>$@

AUTHORS.in:
	( \
	  echo "\@PACKAGE\@ -- authors file.  \@DATE\@" ; \
	  echo "" ; \
	  git log|grep '^Author:'|awk '{if(!authors[$$0]){print$$0;authors[$$0]=1;}}'|tac \
	)>$@

README: README.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

NEWS: NEWS.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

AUTHORS: AUTHORS.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

THANKS: THANKS.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

TODO: TODO.in
	sed -r -e 's:\@PACKAGE\@:$(PACKAGE):g;s:\@VERSION\@:$(VERSION):g;s:\@DATE\@:$(DATE):g' $< >$@

EXTRA_DIST = autogen.sh configure.template \
	README.in NEWS.in THANKS.in TODO.in

DISTCLEANFILES = AUTHORS AUTHORS.in

nobase_dist_share_DATA = \
	grub/fonts/ascii.pf2 \
	grub/fonts/dejavu_10.pf2 \
	grub/fonts/dejavu_12.pf2 \
	grub/fonts/dejavu_14.pf2 \
	grub/fonts/dejavu_16.pf2 \
	grub/fonts/dejavu_18.pf2 \
	grub/fonts/dejavu_22.pf2 \
	grub/fonts/dejavu_24.pf2 \
	grub/fonts/dejavu_bold_10.pf2 \
	grub/fonts/dejavu_bold_12.pf2 \
	grub/fonts/dejavu_bold_14.pf2 \
	grub/fonts/dejavu_bold_16.pf2 \
	grub/fonts/dejavu_bold_18.pf2 \
	grub/fonts/dejavu_bold_22.pf2 \
	grub/fonts/dejavu_bold_24.pf2 \
	grub/fonts/unicode2.pf2 \
	grub/fonts/unicode.pf2 \
	grub/themes/os7live/background.jpg \
	grub/themes/os7live/blob_w.png \
	grub/themes/os7live/boot_menu_c.png \
	grub/themes/os7live/boot_menu_e.png \
	grub/themes/os7live/boot_menu_ne.png \
	grub/themes/os7live/boot_menu_n.png \
	grub/themes/os7live/boot_menu_nw.png \
	grub/themes/os7live/boot_menu_se.png \
	grub/themes/os7live/boot_menu_s.png \
	grub/themes/os7live/boot_menu_sw.png \
	grub/themes/os7live/boot_menu_w.png \
	grub/themes/os7live/dejavu.pf2 \
	grub/themes/os7live/diving.jpg \
	grub/themes/os7live/slider_c.png \
	grub/themes/os7live/slider_n.png \
	grub/themes/os7live/slider_s.png \
	grub/themes/os7live/starfield.png \
	grub/themes/os7live/terminal_box_c.png \
	grub/themes/os7live/terminal_box_e.png \
	grub/themes/os7live/terminal_box_ne.png \
	grub/themes/os7live/terminal_box_n.png \
	grub/themes/os7live/terminal_box_nw.png \
	grub/themes/os7live/terminal_box_se.png \
	grub/themes/os7live/terminal_box_s.png \
	grub/themes/os7live/terminal_box_sw.png \
	grub/themes/os7live/terminal_box_w.png \
	grub/themes/os7live/theme.txt \
	grub/themes/os7live/tower3.png \
	grub/themes/unexicon/blob_w.png \
	grub/themes/unexicon/boot_menu_c.png \
	grub/themes/unexicon/boot_menu_e.png \
	grub/themes/unexicon/boot_menu_ne.png \
	grub/themes/unexicon/boot_menu_n.png \
	grub/themes/unexicon/boot_menu_nw.png \
	grub/themes/unexicon/boot_menu_se.png \
	grub/themes/unexicon/boot_menu_s.png \
	grub/themes/unexicon/boot_menu_sw.png \
	grub/themes/unexicon/boot_menu_w.png \
	grub/themes/unexicon/icons/advanced.png \
	grub/themes/unexicon/icons/autoconsole.png \
	grub/themes/unexicon/icons/boot.png \
	grub/themes/unexicon/icons/cd.png \
	grub/themes/unexicon/icons/checkpoint.png \
	grub/themes/unexicon/icons/copytoram.png \
	grub/themes/unexicon/icons/current.png \
	grub/themes/unexicon/icons/drive.png \
	grub/themes/unexicon/icons/failsafe.png \
	grub/themes/unexicon/icons/fallback.png \
	grub/themes/unexicon/icons/graphical.png \
	grub/themes/unexicon/icons/installed.png \
	grub/themes/unexicon/icons/install.png \
	grub/themes/unexicon/icons/laptop.png \
	grub/themes/unexicon/icons/live.png \
	grub/themes/unexicon/icons/localconsole.png \
	grub/themes/unexicon/icons/makeusb.png \
	grub/themes/unexicon/icons/memtest86.png \
	grub/themes/unexicon/icons/nongraphical.png \
	grub/themes/unexicon/icons/normal.png \
	grub/themes/unexicon/icons/noserial.png \
	grub/themes/unexicon/icons/partition.png \
	grub/themes/unexicon/icons/persist.png \
	grub/themes/unexicon/icons/prepare.png \
	grub/themes/unexicon/icons/previous.png \
	grub/themes/unexicon/icons/recovery.png \
	grub/themes/unexicon/icons/rescue.png \
	grub/themes/unexicon/icons/rollback.png \
	grub/themes/unexicon/icons/serial.png \
	grub/themes/unexicon/icons/settings.png \
	grub/themes/unexicon/slider_c.png \
	grub/themes/unexicon/slider_n.png \
	grub/themes/unexicon/slider_s.png \
	grub/themes/unexicon/splash1.jpg \
	grub/themes/unexicon/splash2.jpg \
	grub/themes/unexicon/splash3.jpg \
	grub/themes/unexicon/splash4.jpg \
	grub/themes/unexicon/splash5.jpg \
	grub/themes/unexicon/terminal_box_c.png \
	grub/themes/unexicon/terminal_box_e.png \
	grub/themes/unexicon/terminal_box_ne.png \
	grub/themes/unexicon/terminal_box_n.png \
	grub/themes/unexicon/terminal_box_nw.png \
	grub/themes/unexicon/terminal_box_se.png \
	grub/themes/unexicon/terminal_box_s.png \
	grub/themes/unexicon/terminal_box_sw.png \
	grub/themes/unexicon/terminal_box_w.png \
	grub/themes/unexicon/theme1.txt \
	grub/themes/unexicon/theme2.txt \
	grub/themes/unexicon/theme3.txt \
	grub/themes/unexicon/theme4.txt \
	grub/themes/unexicon/theme5.txt \
	grub/themes/unexicon/theme6.txt \
	grub/themes/unexicon/theme.txt \
	grub/themes/unexicon/tower3.jpg

