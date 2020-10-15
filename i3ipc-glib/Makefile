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

USES=		gettext \
		gmake \
		gnome \
		libtool \
		pkgconfig

BUILD_DEPENDS=	autotools>=0:devel/autotools \
		gobject-introspection>=0:devel/gobject-introspection \
		gtk-doc>=0:textproc/gtk-doc \
		json-glib>=0:devel/json-glib \
		libxcb>=0:x11/libxcb \
		xcb-proto>=0:x11/xcb-proto

LIB_DEPENDS+=	libjson-glib-1.0.so:devel/json-glib

USE_GNOME+=	glib20
USE_XORG+=	xcb

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--prefix=${DESTDIR}/${GNU_CONFIGURE_PREFIX} MAKE=${GMAKE}
CONFIGURE_SCRIPT=	autogen.sh

INSTALL_TARGET=	install-strip

.include <bsd.port.mk>
