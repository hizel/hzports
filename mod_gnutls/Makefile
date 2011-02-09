# New ports collection makefile for:	mod_fcgid for Apache2
# Date created:		13 August 2004
# Whom:			Akinori MUSHA aka knu <knu@idaemons.org>
#
# $FreeBSD: ports/www/mod_fcgid/Makefile,v 1.22 2010/12/29 20:04:34 pgollucci Exp $
#

PORTNAME=	mod_gnutls
PORTVERSION=	0.5.9
CATEGORIES=	www
MASTER_SITES=	http://www.outoforder.cc/downloads/mod_gnutls/
PKGNAMEPREFIX=	${APACHE_PKGNAMEPREFIX}

MAINTAINER=	hizel@vyborg.ru
COMMENT=	Uses the GnuTLS library to provide SSL, TLS 1.0 encryption for Apache2

LIB_DEPENDS=	gnutls.44:${PORTSDIR}/security/gnutls-devel

LICENSE=	ASL

MAKE_JOBS_SAFE=	yes

USE_BZIP2=	yes
USE_APACHE=	2.0+
HAS_CONFIGURE=		yes
AP_GENPLIST=	yes

SUB_FILES+=     pkg-message
PORTDOCS=	LICENSE NOTICE README README.ENV

post-install:
.if !defined(NOPORTDOCS)
	${MKDIR} ${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${DOCSDIR}
.endif
	@${CAT} ${PKGMESSAGE}

.include <bsd.port.mk>
