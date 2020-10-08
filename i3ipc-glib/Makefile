# $FreeBSD$

PORTNAME=	i3ipc-glib
DISTVERSION=	1.0.1
CATEGORIES=	x11
MASTER_SITES=	https://github.com/altdesktop/i3ipc-glib/releases

MAINTAINER=	robb.randall@gmail.com
COMMENT=	A C interface library to i3wm

LICENSE=		GPLv3
LICENSE_FILE_GPLv3=	${WRKSRC}/COPYING

OPTIONS_DEPENDS=	GLIB
OPTIONS_SINGLE=	X11
OPTIONS_SINGL_X11=	LIBXCB

BUILD_DEPENDS=	gtk-doc>0:textproc/gtk-doc \
		gobject-introspection:devel/gobject-introspection \
		json-glib:devel/json-glib \
		xcb-proto:x11/xcb-proto

USES=	gmake pkgconfig xorg

EXTRACT_SUFX=	.tar.gz
DISTFILES=	v${DISTVERSION}${EXTRACT_SUFX}	
MASTER_SITES=	https://github.com/altdesktop/i3ipc-glib/archive/

USES=	gmake pkgconfig

GNU_CONFIGURE=	yes
CONFIGURE_ENV=	MAKE=gmake
CONFIGURE_ARGS=	--prefix=${DESTDIR}/${GNU_CONFIGURE_PREFIX}
CONFIGURE_SCRIPT=	autogen.sh

.include <bsd.port.mk>
