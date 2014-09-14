#!/usr/bin/scons

env = Environment(platform="win32", tools=["mingw"])


VERSION = "3.0"

CFLAGS = ["-fno-builtin", "-g", "-c", "-W", "-Wreturn-type", "-Wcomment", "-Ilib"]

libgif_source = [
    "lib/egif_lib.c", "lib/dgif_lib.c", "lib/gifalloc.c", "lib/gif_font.c", "lib/gif_hash.c",
    "lib/gif_err.c", "lib/quantize.c", "util/qprintf.c", "util/getarg.c"
]

libgif_a = env.StaticLibrary(source=libgif_source, target="gif", CFLAGS=CFLAGS)

libgif_so = env.SharedLibrary(source=libgif_source, target="giflib", CFLAGS=CFLAGS)

gif2rgb = env.Program(source="util/gif2rgb.c", target="gif2rgb", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifbg = env.Program(source="util/gifbg.c", target="gifbg", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifclrmp = env.Program(source="util/gifclrmp.c", target="gifclrmp", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
giffix = env.Program(source="util/giffix.c", target="giffix", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifhisto = env.Program(source="util/gifhisto.c", target="gifhisto", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifinto = env.Program(source="util/gifinto.c", target="gifinto", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
giftext = env.Program(source="util/giftext.c", target="giftext", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifwedge = env.Program(source="util/gifwedge.c", target="gifwedge", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifecho = env.Program(source="util/gifecho.c", target="gifecho", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifsponge = env.Program(source="util/gifsponge.c", target="gifsponge", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
giffilter = env.Program(source="util/giffilter.c", target="giffilter", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifbuild = env.Program(source="util/gifbuild.c", target="gifbuild", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
gifcolor = env.Program(source="util/gifcolor.c", target="gifcolor", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])
giftool = env.Program(source="util/giftool.c", target="giftool", CFLAGS=CFLAGS, LIBS=["gif"], LIBPATH=["."])

Default([libgif_a, libgif_so, gif2rgb, gifbg, gifclrmp, giffix, gifhisto, gifinto, giftext, gifwedge, gifecho, gifsponge, giffilter, gifbuild, gifcolor, giftool])
