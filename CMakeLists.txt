# This is tested on Linux only.

cmake_minimum_required(VERSION 3.10)
project(minigiac)

# TODO: Add gmp/mpfr detection

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "-fpermissive -std=c++0x")

include_directories(headers)

add_definitions(-DHAVE_NO_HOME_DIRECTORY -DHAVE_SYSCONF -DGIAC_GGB -DIN_GIAC -DHAVE_LIB_PTHREAD
        -DGIAC_GENERIC_CONSTANTS -DHAVE_UNISTD_H -DHAVE_SYS_TIMES_H -DHAVE_SYS_TIME_H -DTIMEOUT
        -DHAVE_MPFR_1 -DHAVE_LIBMPFR -DVERSION="1.2.3")

add_executable(minigiac
        cpp/alg_ext.cc
        cpp/cocoa.cc
        cpp/csturm.cc
        cpp/derive.cc
        cpp/desolve.cc
        cpp/ezgcd.cc
        cpp/freeglut_stroke_roman.c
        cpp/gauss.cc
        cpp/gausspol.cc
        cpp/gen.cc
        cpp/global.cc
        cpp/help.cc
        cpp/identificateur.cc
        cpp/ifactor.cc
        cpp/index.cc
        cpp/input_lexer.cc
        cpp/input_parser.cc
        cpp/intg.cc
        cpp/intgab.cc
        cpp/isom.cc
        cpp/lin.cc
        cpp/maple.cc
        cpp/mathml.cc
        cpp/misc.cc
        cpp/modfactor.cc
        cpp/modpoly.cc
        cpp/moyal.cc
        cpp/opengl.cc
        cpp/pari.cc
        cpp/permu.cc
        cpp/plot.cc
        cpp/plot3d.cc
        cpp/prog.cc
        cpp/quater.cc
        cpp/risch.cc
        cpp/rpn.cc
        cpp/series.cc
        cpp/solve.cc
        cpp/sparse.cc
        cpp/subst.cc
        cpp/sym2poly.cc
        cpp/symbolic.cc
        cpp/tex.cc
        cpp/threaded.cc
        cpp/ti89.cc
        cpp/tinymt32.cc
        cpp/TmpFGLM.cpp
        cpp/TmpLESystemSolver.cpp
        cpp/unary.cc
        cpp/usual.cc
        cpp/vecteur.cc
        headers/android/gmp.h
        headers/android/mpfr.h
        headers/alg_ext.h
        headers/cocoa.h
        headers/config.h
        headers/csturm.h
        headers/derive.h
        headers/desolve.h
        headers/dispatch.h
        headers/ezgcd.h
        headers/fac_table.h
        headers/fib_table.h
        headers/first.h
        headers/fits_s.h
        headers/fits_u.h
        headers/fraction.h
        headers/gauss.h
        headers/gausspol.h
        headers/gen.h
        headers/gen_inverse.h
        headers/giac.h
        headers/giacintl.h
        headers/giacPCH.h
        headers/global.h
        headers/gmp-mparam.h
        headers/gmp.h
        headers/gmp_replacements.h
        headers/gmpxx.h
        headers/help.h
        headers/identificateur.h
        headers/ieee_floats.h
        headers/ifactor.h
        headers/index.h
        headers/input_lexer.h
        headers/input_parser.h
        headers/intg.h
        headers/intgab.h
        headers/isom.h
        headers/lexer.h
        headers/lexer_tab_int.h
        headers/lin.h
        headers/longlong.h
        headers/maple.h
        headers/mathml.h
        headers/misc.h
        headers/modfactor.h
        headers/modpoly.h
        headers/monomial.h
        headers/moyal.h
        headers/mp_bases.h
        headers/mparam.h
        headers/mpf2mpfr.h
        headers/mpfr-gmp.h
        headers/mpfr-impl.h
        headers/mpfr-intmax.h
        headers/mpfr-longlong.h
        headers/mpfr-thread.h
        headers/mpfr.h
        headers/opengl.h
        headers/pari.h
        headers/path.h
        headers/permu.h
        headers/plot.h
        headers/plot3d.h
        headers/poly.h
        headers/prog.h
        headers/quater.h
        headers/risch.h
        headers/rpn.h
        headers/series.h
        headers/solve.h
        headers/sparse.h
        headers/static.h
        headers/static_extern.h
        headers/static_help.h
        headers/static_lexer.h
        headers/static_lexer_.h
        headers/subst.h
        headers/sym2poly.h
        headers/symbolic.h
        headers/tex.h
        headers/threaded.h
        headers/ti89.h
        headers/tinymt32.h
        headers/tinymt32_license.h
        headers/TmpFGLM.H
        headers/TmpLESystemSolver.H
        headers/trialdivtab.h
        headers/unary.h
        headers/usual.h
        headers/vecteur.h
        headers/vector.h
        minigiac/minigiac.cc)

target_link_libraries(minigiac gmp mpfr)


