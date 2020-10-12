# $FreeBSD$

PORTNAME=	i3ipc-glib
DISTVERSION=	1.0.1
CATEGORIES=	x11
MASTER_SITES=	https://github.com/altdesktop/i3ipc-glib/releases/
DISTFILES=	v${DISTVERSION}${EXTRACT_SUFX}

MAINTAINER=	robb.randall@gmail.com
COMMENT=	C interface library to i3wm

LICENSE=	GPLv3
LICENSE_FILE_GPLv3=	${WRKSRC}/COPYING

BUILD_DEPENDS=	glib:devel/glib \
		gobject-introspection:devel/gobject-introspection \
		gtk-doc:textproc/gtk-doc \
		json-glib:devel/json-glib \
		libxcb:x11/libxcb \
		xcb-proto:x11/xcb-proto

USES=		gmake pkgconfig gettext
PLIST+=		NLS=""

GNU_CONFIGURE=	yes
CONFIGURE_ENV=	MAKE=gmake
CONFIGURE_ARGS=	--prefix=${DESTDIR}/${GNU_CONFIGURE_PREFIX}
CONFIGURE_SCRIPT=	autogen.sh

.include <bsd.port.mk>
