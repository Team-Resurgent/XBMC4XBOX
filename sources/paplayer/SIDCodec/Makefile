CFLAGS=-D_LINUX -DHAVE_UNIX -DHAVE_STRCASECMP -DHAVE_STRNCASECMP -DHAVE_IOS_OPENMODE -fPIC -Ilibsidplay/win/VC -Ibuilders/resid-builder/include/sidplay/builders -Ilibsidplay/include/sidplay -Iresid -Ilibsidplay/include -I../../../XBMC/xbmc/linux -I../../../XBMC/xbmc
OBJS=libsidplay/src/mos6510/mos6510.o libsidplay/src/mos6526/mos6526.o libsidplay/src/mos656x/mos656x.o  libsidplay/src/sid6526/sid6526.o libsidplay/src/sidtune/IconInfo.o libsidplay/src/sidtune/InfoFile.o libsidplay/src/sidtune/MUS.o libsidplay/src/sidtune/p00.o libsidplay/src/sidtune/PP20.o libsidplay/src/sidtune/prg.o libsidplay/src/sidtune/PSID.o libsidplay/src/sidtune/SidTune.o libsidplay/src/sidtune/SidTuneTools.o libsidplay/src/xsid/xsid.o libsidplay/src/config.o resid/envelope.o libsidplay/src/event.o resid/extfilt.o resid/filter.o libsidplay/src/mixer.o libsidplay/src/player.o resid/pot.o libsidplay/src/psiddrv.o libsidplay/src/reloc65.o builders/resid-builder/src/resid-builder.o builders/resid-builder/src/resid.o resid/sid.o libsidplay/src/sidplay2.o resid/version.o resid/voice.o resid/wave.o resid/wave6581__ST.o resid/wave6581_P_T.o resid/wave6581_PS_.o resid/wave6581_PST.o resid/wave8580__ST.o resid/wave8580_P_T.o resid/wave8580_PS_.o resid/wave8580_PST.o libsidplay/win/VC/XBMCSID.o

libsidplay2-i486-linux.so: $(OBJS)
	gcc -fPIC -shared -o $@ $(OBJS) `cat ../../../XBMC/xbmc/cores/DllLoader/exports/wrapper.def` ../../../XBMC/xbmc/cores/DllLoader/exports/wrapper.o

clean:
	$(RM) $(OBJS) *.so

%o : %c
	gcc $(CFLAGS) -O2 -fPIC -c $< -o $@

%o : %cpp
	g++ $(CFLAGS) -O2 -fPIC -c $< -o $@

%o : %cc
	g++ $(CFLAGS) -O2 -fPIC -c $< -o $@
