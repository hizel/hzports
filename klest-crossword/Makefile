# Created by: hizel
# $FreeBSD$

PORTNAME=	klest-crossword
PORTVERSION=	1.2.3
CATEGORIES=	games
MASTER_SITES=	SF/${PORTNAME}/${PORTVERSION}
DISTNAME=	${PORTNAME}-${PORTVERSION}-src

MAINTAINER=	ports@FreeBSD.org
COMMENT=	game for professional compiling, editing and easy guessing american and classic the crossword puzzles

LICENSE=	GPLv2

USES=		gmake qmake
USE_QT4=	gui sql network webkit moc_build qmake_build rcc_build uic_build

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/usr/games/${PORTNAME}-${PORTVERSION} ${STAGEDIR}${PREFIX}/bin
	(cd ${WRKSRC}/usr/share && ${COPYTREE_SHARE} \* ${STAGEDIR}${PREFIX}/share/)

.include <bsd.port.mk>
