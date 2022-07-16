@ -1,110 +0,0 @@
#ICC		= xcrun -sdk iphoneos clang
MCC		= clang
MCC_FLAGS	= -I./include -Os -Wall

LIBS		= */*.a -lz -lpng -lbz2 -lcrypto

test: asr iboot kernel common hfs minizip ipsw-patch
	$(MCC) $(MCC_FLAGS) $(LIBS) tools/kernel_patcher.c -o tools/kernel_patcher
	strip tools/kernel_patcher
	$(MCC) $(MCC_FLAGS) $(LIBS) tools/iboot_patcher.c -o tools/iboot_patcher
	strip tools/iboot_patcher
	$(MCC) $(MCC_FLAGS) $(LIBS) tools/asr_patcher.c -o tools/asr_patcher
	strip tools/asr_patcher
	$(MCC) $(MCC_FLAGS) $(LIBS) tools/iboot_tester.c -o tools/iboot_tester
	strip tools/iboot_tester
