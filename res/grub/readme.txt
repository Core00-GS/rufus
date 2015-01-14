This directory contains the Grub4DOS boot records that are used by Rufus

* grldr.mbr was compiled on Linux Debian 7.7.0 x64, using gcc-multilib 4.7.2, from
  https://github.com/chenall/grub4dos/commit/8549aae.

* Note that, for convenience reasons, the first 512 bytes from this grldr.mbr are
  *not* the ones that Rufus processes when writing the actual MBR (first 512 bytes).
  Instead, the byte array from src/ms-sys/inc/mbr_grub.h (whose content is identical)
  is what Rufus uses. If you have modified this file, and the MBR section is altered,
  be mindful that you also need to update the array in mbr_grub.h.

* For details, see src/format.c, src/msys/br.c and src/msys/inc/mbr_grub.h.