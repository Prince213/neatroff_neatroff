cmake_minimum_required(VERSION 3.0)
project(neatroff C)
set(FDIR "${CMAKE_INSTALL_PREFIX}/share/neatroff/font" CACHE PATH "Default font directory")
set(MDIR "${CMAKE_INSTALL_PREFIX}/share/neatroff/tmac" CACHE PATH "Default macro directory")
add_compile_definitions("TROFFFDIR=\"${FDIR}\"" "TROFFMDIR=\"${MDIR}\"")
add_executable(roff roff.c dev.c font.c in.c cp.c tr.c ren.c out.c reg.c sbuf.c fmt.c eval.c draw.c wb.c hyph.c map.c clr.c char.c dict.c iset.c dir.c)
install(TARGETS roff)
