# $FreeBSD$

PORTNAME=       i3ipc-glib
DISTVERSION=    1.0.1
CATEGORIES=     x11
MASTER_SITES=   https://github.com/altdesktop/i3ipc-glib/archive/
DISTFILES=      v${DISTVERSION}${EXTRACT_SUFX}

MAINTAINER=     robb.randall@gmail.com
COMMENT=        C interface library to i3wm

LICENSE=        GPLv3
LICENSE_FILE_GPLv3=     ${WRKSRC}/COPYING

LIB_DEPENDS=	devel/glib20 \
		glib.h:devel/glib20 \
		gprintf.h:devel/glib20 \
		json-glib.h:devel/json-glib \
		glib-object.h:devel/gobject-introspection 

BUILD_DEPENDS=	gobject-introspection:devel/gobject-introspection \
		gtk-doc:textproc/gtk-doc \
		json-glib:devel/json-glib \
		libxcb:x11/libxcb \
		xcb-proto:x11/xcb-proto

RUN_DEPENDS=    ${BUILD_DEPENDS}

USES=           gmake pkgconfig gettext
PLIST+=         NLS=""
OPTIONS_DEFINE=	GLIB
GNU_CONFIGURE=	yes
CONFIGURE_ENV=	MAKE=gmake
CONFIGURE_ARGS=	--prefix=${DESTDIR}/${GNU_CONFIGURE_PREFIX}
CONFIGURE_SCRIPT=	autogen.sh

.include <bsd.port.mk>
