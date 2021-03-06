# -*- make -*-
#
# Makefile, overall Makefile for CVS sources.
#
# Makefile.  Generated from Makefile.in by configure.
# 
# $Id: Makefile.in,v 1.71 2006/06/20 17:02:52 dors Exp $




MAKE_LOGIN=@echo Skipping $(MAKE)
MAKE_APACHE=$(MAKE)

CC=gcc

prefix=$(DESTDIR)/usr/local/pubcookie
srcdir=.
builddir=.

PUBCOOKIE_DIR=$(prefix)
KEY_DIR=$(PUBCOOKIE_DIR)/keys
TEMPLATE_DIR=$(PUBCOOKIE_DIR)/login_templates
LOGIN_DIR=$(PUBCOOKIE_DIR)/login
CERT_DB_DIR=$(PUBCOOKIE_DIR)/keys
LOGIN_MEDIA_DIR=$(PUBCOOKIE_DIR)/login/media

CERT_DB_SOURCE=

INSTALL=/usr/bin/install -c
INSTALL_BIN=$(INSTALL) -m 755
INSTALL_OTHER=$(INSTALL) -m 644
INSTALL_DIR=$(INSTALL) -d

RM=/bin/rm
FORCE_RM=$(RM) -f
RECURSIVE_FORCE_RM=$(RM) -rf
CP=/bin/cp
RECURSIVE_CP=$(CP) -r
MKDIR=/bin/mkdir
MV=/bin/mv
AWK=mawk
SED=/bin/sed
TAR=/bin/tar
GZIP=/bin/gzip
CHMOD=/bin/chmod
TEST=/usr/bin/test

LIBS=-lssl -lcrypto -ldl -lnsl  -lgcc
CPPFLAGS= -I/usr/include/openssl -DHAVE_CONFIG_H -DLOGIN_SERVER -I$(builddir)/src 
CFLAGS=-g -O2 $(CPPFLAGS)
LDFLAGS= -L/usr/lib/gcc/x86_64-linux-gnu/4.4.3 $(LIBS)
LOGINLIBS=-lssl -lcrypto -ldl -lnsl  -lgcc 

APXS=/usr/bin/apxs2

CONFIGURE_TMP_FILES=$(builddir)/config.status \
					$(builddir)/config.log \
					$(builddir)/src/config.h \
					$(builddir)/Makefile \
					$(builddir)/src/pbc_path.h \
					$(builddir)/src/pbc_version.h \
					$(builddir)/src/Win32/PubCookieFilter.h \
					$(builddir)/src/Win32/PubCookieFilter.rc \
					$(builddir)/stamp-h

CONFIGURE_TMP_DIRS=$(srcdir)/autom4te.cache

CONFIGURE_FILES=$(srcdir)/configure \
				$(srcdir)/configure.ac \
				$(srcdir)/Makefile.in \
				$(srcdir)/Makefile.in.ap1 \
				$(srcdir)/Makefile.in.ap2 \
				$(srcdir)/Makefile.tmpl.in \
				$(srcdir)/modules.mk \
				$(srcdir)/install-sh \
				$(srcdir)/config.sub \
				$(srcdir)/config.guess \
				$(srcdir)/aclocal.m4 \
				$(srcdir)/stamp-h.in

SRC_CONFIGURE_FILES=$(srcdir)/src/config.h.in \
					$(srcdir)/src/pbc_path.h.in \
					$(srcdir)/src/pbc_version.h.in 

TEST_SRC=$(srcdir)/src/pbc_create.c \
		 $(srcdir)/src/pbc_verify.c \
		 $(srcdir)/src/check_crypted_blob.c \
		 $(srcdir)/src/what_is_my_ip.c

TEST_FILES=pbc_create pbc_verify check_crypted_blob \
		   verify what_is_my_ip

UTIL_SRC=$(srcdir)/src/keyserver.c \
		 $(srcdir)/src/keyclient.c

VERIFIERS=$(builddir)/src/verify_alwaystrue.o \
		  $(builddir)/src/verify_fork.o \
		  $(builddir)/src/verify_kerberos4.o \
		  $(builddir)/src/verify_kerberos5.o \
		  $(builddir)/src/verify_shadow.o \
		  $(builddir)/src/verify_uwsecurid.o \
		  $(builddir)/src/verify_ldap.o \
		   \
		  $(builddir)/src/verify.o

VERIFY_SRC=$(srcdir)/src/verify.c \
		    \
		   $(srcdir)/src/verify_alwaystrue.c \
		   $(srcdir)/src/verify_fork.c \
		   $(srcdir)/src/verify_kerberos4.c \
		   $(srcdir)/src/verify_kerberos5.c \
		   $(srcdir)/src/verify_shadow.c \
		   $(srcdir)/src/verify_uwsecurid.c \
		   $(srcdir)/src/verify_ldap.c

FLAVOR_SRC=$(srcdir)/src/flavor.c \
		   $(srcdir)/src/ntmpl.c \
		    \
		   $(srcdir)/src/flavor_basic.c \
		   $(srcdir)/src/flavor_uwsecurid.c \
		   $(srcdir)/src/flavor_getcred.c

INDEX_OBJ=$(builddir)/src/index.cgi.o $(builddir)/src/flavor.o \
		  $(builddir)/src/flavor_basic.o \
		  $(builddir)/src/flavor_getcred.o \
		  $(builddir)/src/flavor_uwsecurid.o \
		  $(builddir)/src/ntmpl.o \
		   \
		  $(VERIFIERS)

INDEX_FILES=$(builddir)/index.cgi

INDEX_SRC=$(srcdir)/src/index.cgi.c \
		   \
		  $(VERIFY_SRC) \
		  $(FLAVOR_SRC)

KEYMGT_FILES=keyclient keyserver

KEYMGT_SRC=$(srcdir)/src/keyclient.c $(srcdir)/src/keyserver.c

INDEX_HEAD=$(srcdir)/src/index.cgi.h \
		   $(srcdir)/src/flavor.h \
		   $(srcdir)/src/verify.h \
		   $(srcdir)/src/snprintf.h

LIB_HEAD=$(srcdir)/src/pbc_config.h \
		 $(srcdir)/src/pubcookie.h \
		 $(srcdir)/src/libpubcookie.h \
		 $(srcdir)/src/pbc_version.h \
		 $(srcdir)/src/pbc_myconfig.h \
		 $(srcdir)/src/security.h \
		 $(srcdir)/src/pbc_logging.h \
		 $(srcdir)/src/strlcpy.h \
		 $(srcdir)/src/snprintf.h \
		 $(srcdir)/src/pbc_configure.h \
		 $(srcdir)/src/pbc_time.h


LIB_SRC=$(srcdir)/src/libpubcookie.c \
		$(srcdir)/src/base64.c \
		$(srcdir)/src/strlcpy.c \
		 \
		$(srcdir)/src/pbc_myconfig.c \
		$(srcdir)/src/security_legacy.c \
		$(srcdir)/src/pbc_logging.c \
		$(srcdir)/src/capture_cmd_output.c \
		$(srcdir)/src/pbc_configure.c \
		$(srcdir)/src/pbc_time.c

LIB_OBJ=$(builddir)/src/libpubcookie.o \
		$(builddir)/src/base64.o \
		$(builddir)/src/strlcpy.o \
		 \
		$(builddir)/src/pbc_myconfig.o \
		$(builddir)/src/security_legacy.o \
		$(builddir)/src/pbc_logging.o \
		$(builddir)/src/capture_cmd_output.o \
		$(builddir)/src/pbc_configure.o \
		$(builddir)/src/pbc_time.o

MOD_SRC=$(srcdir)/src/mod_pubcookie.c \
        $(srcdir)/src/pbc_apacheconfig.c

MOD_HEAD=$(srcdir)/src/mod_pubcookie.h \
		 $(srcdir)/src/html.h \
		 $(srcdir)/src/pbc_apacheconfig.h

LIB_TESTS=base64 pbc_myconfig myconf

LOGIN_TEMPLATES=$(srcdir)/src/login_templates.generic/copyright \
                $(srcdir)/src/login_templates.generic/error \
		$(srcdir)/src/login_templates.generic/form_expired \
		$(srcdir)/src/login_templates.generic/login \
		$(srcdir)/src/login_templates.generic/login_auth_prob_uwsecurid \
		$(srcdir)/src/login_templates.generic/login_bad_auth \
		$(srcdir)/src/login_templates.generic/login_bad_auth_static_user \
		$(srcdir)/src/login_templates.generic/login_bad_auth_static_user \
		$(srcdir)/src/login_templates.generic/login_bad_auth_static_user \
		$(srcdir)/src/login_templates.generic/login_cache_creds_wrong \
		$(srcdir)/src/login_templates.generic/login_expired \
		$(srcdir)/src/login_templates.generic/login_next_prn \
		$(srcdir)/src/login_templates.generic/login_expired \
		$(srcdir)/src/login_templates.generic/login_nolcookie \
		$(srcdir)/src/login_templates.generic/login_pass_form_field \
		$(srcdir)/src/login_templates.generic/login_pass_static \
		$(srcdir)/src/login_templates.generic/login_pinit \
		$(srcdir)/src/login_templates.generic/login_reauth \
		$(srcdir)/src/login_templates.generic/login_unauth_grant \
		$(srcdir)/src/login_templates.generic/login_user_form_field \
		$(srcdir)/src/login_templates.generic/login_user_hidden \
		$(srcdir)/src/login_templates.generic/login_user_static \
		$(srcdir)/src/login_templates.generic/login_uwsecurid \
		$(srcdir)/src/login_templates.generic/logo \
		$(srcdir)/src/login_templates.generic/logout_already_weblogin \
		$(srcdir)/src/login_templates.generic/logout_app \
		$(srcdir)/src/login_templates.generic/logout_app_custom \
		$(srcdir)/src/login_templates.generic/logout_part1 \
		$(srcdir)/src/login_templates.generic/logout_part2 \
		$(srcdir)/src/login_templates.generic/logout_postscript_still_others \
		$(srcdir)/src/login_templates.generic/logout_postscript_still_weblogin \
		$(srcdir)/src/login_templates.generic/logout_still_known \
		$(srcdir)/src/login_templates.generic/logout_still_weblogin \
		$(srcdir)/src/login_templates.generic/logout_time_remaining \
		$(srcdir)/src/login_templates.generic/logout_weblogin \
		$(srcdir)/src/login_templates.generic/nonpost_redirect \
		$(srcdir)/src/login_templates.generic/notok \
		$(srcdir)/src/login_templates.generic/notok_badagent \
		$(srcdir)/src/login_templates.generic/notok_form_multipart \
		$(srcdir)/src/login_templates.generic/notok_generic \
		$(srcdir)/src/login_templates.generic/notok_need_ssl \
		$(srcdir)/src/login_templates.generic/pinit_response1 \
		$(srcdir)/src/login_templates.generic/pinit_response2 \
		$(srcdir)/src/login_templates.generic/status \
		$(srcdir)/src/login_templates.generic/welcome_back \
		$(srcdir)/src/login_templates.generic/README


LOGIN_MEDIA=$(srcdir)/src/login_templates.generic/media/pubcookie.css \
			 $(srcdir)/src/login_templates.generic/media/check.gif \
			 $(srcdir)/src/login_templates.generic/media/icon-excl.gif \
			 $(srcdir)/src/login_templates.generic/media/icon-time.gif

DOCS=$(srcdir)/doc/config.html \
	 $(srcdir)/doc/CREDITS.txt \
	 $(srcdir)/doc/CHANGES.txt \
	 $(srcdir)/doc/LICENSE.txt \
	 $(srcdir)/doc/starter.key \
	 $(srcdir)/doc/config.sample \
	 $(srcdir)/doc/config.login.sample \
	 $(srcdir)/doc/install-mod_pubcookie.html \
	 $(srcdir)/doc/mod_pubcookie-directives.html \
	 $(srcdir)/doc/install-login.html \
	 $(srcdir)/doc/install-filter.html \
	 $(srcdir)/doc/krb5-getcred.html \
	 $(srcdir)/doc/HACKING.txt \
	 $(srcdir)/doc/pubcookie.css

CGIC_FILES=$(srcdir)/cgic/Makefile.in \
		   $(srcdir)/cgic/capture.c \
		   $(srcdir)/cgic/cgic.c \
		   $(srcdir)/cgic/cgic.h \
		   $(srcdir)/cgic/cgic.html \
		   $(srcdir)/cgic/cgic.txt \
		   $(srcdir)/cgic/cgictest.c \
		   $(srcdir)/cgic/license.txt \
		   $(srcdir)/cgic/readme.txt \
		   $(srcdir)/cgic/support.txt \
		   $(srcdir)/cgic/testform.html \
		   $(srcdir)/cgic/CHANGES

VERSION = `echo 3.3.4a | $(SED) "s/ /-/g" `

BASENAME = pubcookie
DISTNAME = $(BASENAME)-$(VERSION)

# PHONY before 'all' causes aix make to make .PHONY
all: $(builddir)/Makefile  keyclient apache_module

.PHONY: all clean install dist login_server apache_module ver aix_warning


.c.o:
	$(CC) -c $(CFLAGS) $< -o $@

$(srcdir)/configure: # $(srcdir)/configure.ac $(srcdir)/aclocal.m4
	cd $(srcdir) && $(RECURSIVE_FORCE_RM) $(CONFIGURE_TMP_DIRS)
	$(FORCE_RM) $(srcdir)/configure
	cd $(srcdir) && autoconf $(srcdir)/configure.ac > $(srcdir)/configure
	$(CHMOD) +x $(srcdir)/configure

# autoheader might not change config.h.in, so touch a stamp file.
$(srcdir)/src/config.h.in: # $(srcdir)/stamp-h.in
$(srcdir)/stamp-h.in: # $(srcdir)/configure.ac
	cd $(srcdir) && autoheader $(srcdir)/configure.ac
	date > $(srcdir)/stamp-h.in

$(builddir)/src/config.h: $(builddir)/stamp-h
$(builddir)/src/pbc_path.h: $(builddir)/stamp-h
$(builddir)/src/pbc_version.h: $(builddir)/stamp-h
$(builddir)/src/Win32/PubCookieFilter.h: $(builddir)/stamp-h
$(builddir)/src/Win32/PubCookieFilter.rc: $(builddir)/stamp-h
$(builddir)/stamp-h: $(srcdir)/src/config.h.in $(srcdir)/src/pbc_path.h.in $(srcdir)/src/pbc_version.h.in $(srcdir)/src/Win32/PubCookieFilter.h.in $(srcdir)/src/Win32/PubCookieFilter.rc.in $(builddir)/config.status
	$(builddir)/config.status

$(builddir)/Makefile: $(srcdir)/Makefile.in $(builddir)/src/config.h $(builddir)/config.status
	$(builddir)/config.status

$(builddir)/config.status: $(srcdir)/configure
	$(builddir)/config.status --recheck

# $(builddir)/src/%.o: $(srcdir)/src/%.c
# 	$(CC) $(CFLAGS) -o $@ -c $<

login_server: no_login l_ver $(INDEX_FILES) $(KEYMGT_FILES)

no_login:
	@echo "The login server is not configured"
	@bomb

l_ver:
	@echo Making $(DISTNAME) login server;

a_ver:
	@echo Making $(DISTNAME) apache module;

candv:	$(builddir)/src/candv.o $(LIB_OBJ)
	$(CC) $(CFLAGS) -o $@ $(builddir)/src/candv.o $(LIB_OBJ) $(LDFLAGS)

dtest:	$(builddir)/src/dtest.o $(LIB_OBJ)
	$(CC) $(CFLAGS) -o $@ $(builddir)/src/dtest.o $(LIB_OBJ) $(LDFLAGS)

ntmpl_test: $(srcdir)/src/ntmpl.c $(LIB_OBJ)
	$(CC) ${CFLAGS} -DTEST_NTMPL -o $@ $(srcdir)/src/ntmpl.c $(LIB_OBJ) $(LDFLAGS) $(EXTRA_LIBS)

check_crypted_blob:	$(builddir)/src/check_crypted_blob.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/check_crypted_blob.o $(LIB_OBJ) $(LDFLAGS)

pbc_create:	$(builddir)/src/pbc_create.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/pbc_create.o $(LIB_OBJ) $(LDFLAGS)

pbc_verify:	$(builddir)/src/pbc_verify.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/pbc_verify.o $(LIB_OBJ) $(LDFLAGS)

pbc_key_generic: $(builddir)/src/pbc_key_generic.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/pbc_key_generic.o $(LIB_OBJ) $(LDFLAGS)

pbc_key_local: $(builddir)/src/pbc_key_local.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/pbc_key_local.o $(LIB_OBJ) $(LDFLAGS)

make_crypted_blob: $(builddir)/src/make_crypted_blob.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/make_crypted_blob.o $(LIB_OBJ) $(LDFLAGS)

what_is_my_ip: $(builddir)/src/what_is_my_ip.o $(LIB_OBJ)
	$(CC) ${CFLAGS} -o $@ $(builddir)/src/what_is_my_ip.o $(LIB_OBJ) $(LDFLAGS)

$(builddir)/index.cgi: $(builddir)/cgic/libcgic.a $(LIB_OBJ) $(INDEX_OBJ)
	$(CC) ${CFLAGS} -o $@ $(INDEX_OBJ) $(LIB_OBJ) $(LDFLAGS) $(LOGINLIBS)

$(builddir)/cgic/libcgic.a:
	@echo "Making all in cgic"
	(cd $(builddir)/cgic; $(MAKE))

$(INDEX_OBJ): $(LIB_HEAD) $(INDEX_HEAD) $(builddir)/src/pbc_path.h $(srcdir)/src/pbc_version.h $(builddir)/src/config.h

keyserver: $(builddir)/src/keyserver.o $(LIB_OBJ)
	$(CC) $(CFLAGS) -o $@ $(builddir)/src/keyserver.o $(LIB_OBJ) $(LDFLAGS) $(LOGINLIBS)

keyclient: $(builddir)/src/keyclient.o $(LIB_OBJ)
	$(CC) $(CFLAGS) -o $@ $(builddir)/src/keyclient.o $(LIB_OBJ) $(LDFLAGS) $(LOGINLIBS)


# Installation Targets

install: $(KEY_DIR)  install-apache 
	$(INSTALL_BIN) keyclient $(PUBCOOKIE_DIR)

install-login: no_login $(LOGIN_DIR) $(TEMPLATE_DIR) $(TEMPLATE_DIR).default $(LOGIN_TEMPLATES) $(LOGIN_MEDIA_DIR) $(TEMPLATE_DIR).default/media $(LOGIN_MEDIA) login_server
	@for file in $(INDEX_FILES); do \
		echo $(INSTALL_BIN) $$file $(LOGIN_DIR); \
		$(INSTALL_BIN) $$file $(LOGIN_DIR); \
	done
	@for file in $(LOGIN_TEMPLATES); do \
		echo $(INSTALL_OTHER) $$file $(TEMPLATE_DIR).default; \
		$(INSTALL_OTHER) $$file $(TEMPLATE_DIR).default; \
	done
	@for file in $(LOGIN_TEMPLATES); do \
		bfile=`basename $$file`; \
		$(TEST) ! -f $(TEMPLATE_DIR)/$$bfile && \
		 	echo $(INSTALL_OTHER) $$file $(TEMPLATE_DIR) && \
			$(INSTALL_OTHER) $$file $(TEMPLATE_DIR); \
		true; \
	done
	@for file in $(LOGIN_MEDIA); do \
		echo $(INSTALL_OTHER) $$file $(TEMPLATE_DIR).default/media; \
		$(INSTALL_OTHER) $$file $(TEMPLATE_DIR).default/media; \
	done
	@for file in $(LOGIN_MEDIA); do \
		bfile=`basename $$file`; \
		$(TEST) ! -f $(LOGIN_MEDIA_DIR)/$$bfile && \
			echo $(INSTALL_OTHER) $$file $(LOGIN_MEDIA_DIR) && \
			$(INSTALL_OTHER) $$file $(LOGIN_MEDIA_DIR); \
		true; \
	done
	@for file in $(KEYMGT_FILES); do \
		echo $(INSTALL_BIN) $$file $(PUBCOOKIE_DIR); \
		$(INSTALL_BIN) $$file $(PUBCOOKIE_DIR); \
	done
	@for file in $(CERT_DB_SOURCE)/cert7.db $(CERT_DB_SOURCE)/key3.db; do \
		$(TEST) "x$(CERT_DB_SOURCE)" != "x" && \
			echo $(INSTALL_OTHER) $$file $(CERT_DB_DIR) && \
			$(INSTALL_OTHER) $$file $(CERT_DB_DIR); \
		true; \
	done
	$(INSTALL_OTHER) doc/starter.key $(PUBCOOKIE_DIR)
	$(INSTALL_OTHER) doc/config.login.sample $(PUBCOOKIE_DIR)
	@$(TEST) ! -f $(PUBCOOKIE_DIR)/config && \
		echo $(INSTALL_OTHER) doc/config.login.sample \
			 $(PUBCOOKIE_DIR)/config && \
		$(INSTALL_OTHER) doc/config.login.sample $(PUBCOOKIE_DIR)/config; \
		true

install-apache: 
	@echo "Making all in module"
	(cd module; $(MAKE) install)

$(PUBCOOKIE_DIR):
	$(INSTALL_DIR) $(PUBCOOKIE_DIR)

$(KEY_DIR): $(PUBCOOKIE_DIR)
	$(INSTALL_DIR) $(KEY_DIR)

$(LOGIN_DIR): $(PUBCOOKIE_DIR)
	$(INSTALL_DIR) $(LOGIN_DIR)

#$(LOGIN_IMG_DIR): $(PUBCOOKIE_DIR)
#	$(INSTALL_DIR) $(LOGIN_IMG_DIR)
$(LOGIN_MEDIA_DIR): $(PUBCOOKIE_DIR)
	$(INSTALL_DIR) $(LOGIN_MEDIA_DIR)

$(TEMPLATE_DIR): $(PUBCOOKIE_DIR)
	$(INSTALL_DIR) $(TEMPLATE_DIR)

$(TEMPLATE_DIR).default: $(PUBCOOKIE_DIR)
	$(INSTALL_DIR) $(TEMPLATE_DIR).default

$(TEMPLATE_DIR).default/media: $(TEMPLATE_DIR).default
	$(INSTALL_DIR) $(TEMPLATE_DIR).default/media

$(LIB_OBJ): $(LIB_HEAD) $(builddir)/src/pbc_path.h $(srcdir)/src/pbc_version.h.in $(builddir)/src/config.h

# Test Targets

test:: verify
	touch vtest
	./verify alwaystrue nobody nothing

verify: $(VERIFY_SRC) $(LIB_OBJ) $(builddir)/cgic/libcgic.a
	$(CC) $(CFLAGS) -o verify -DTEST_VERIFY $(VERIFY_SRC) $(LDFLAGS) $(LIB_OBJ) $(LOGINLIBS)

tests: $(TEST_FILES)

test:: base64 myconf pbc_myconfig
	cat base64 | ./base64
	./pbc_myconfig

myconf:
	echo "foo: hi hi2" > myconf

base64: $(srcdir)/src/base64.c
	$(CC) $(CFLAGS) -o base64 -DTEST_BASE64 $(srcdir)/src/base64.c $(LDFLAGS) $(LOGINLIBS)

pbc_myconfig: $(srcdir)/src/pbc_myconfig.c
	$(CC) $(CFLAGS) -o pbc_myconfig -DTEST_MYCONFIG $(srcdir)/src/pbc_myconfig.c $(LDFLAGS) $(LOGINLIBS)

# Cleanup targets

clean::
	-$(FORCE_RM) $(builddir)/*.so $(builddir)/src/*.so $(builddir)/so_locations
	-$(FORCE_RM) $(builddir)/*.la
	-$(FORCE_RM) $(INDEX_FILES) $(builddir)/*.o $(builddir)/src/*.o
	-$(FORCE_RM) $(TEST_FILES) $(KEYMGT_FILES)
	-$(FORCE_RM) pbc_myconfig myconf base64
	(cd $(builddir)/cgic; $(MAKE) clean)
	(cd $(builddir)/module; $(MAKE) clean)

distclean:: clean
	$(FORCE_RM) $(CONFIGURE_TMP_FILES)
	$(RECURSIVE_FORCE_RM) $(CONFIGURE_TMP_DIRS)
	(cd $(builddir)/cgic; $(MAKE) distclean)

# APXS Stuff.

apache_module: 
	(cd module; $(MAKE))

no_module:
	@echo "The apache module is not configured."
	@bomb

# Win32 ... Nothing here except the Dist files.

WIN32_SSL_SRC=$(srcdir)/src/Win32/include/openssl/aes.h \
			$(srcdir)/src/Win32/include/openssl/asn1.h \
			$(srcdir)/src/Win32/include/openssl/asn1_mac.h \
			$(srcdir)/src/Win32/include/openssl/asn1t.h \
			$(srcdir)/src/Win32/include/openssl/bio.h \
			$(srcdir)/src/Win32/include/openssl/blowfish.h \
			$(srcdir)/src/Win32/include/openssl/bn.h \
			$(srcdir)/src/Win32/include/openssl/buffer.h \
			$(srcdir)/src/Win32/include/openssl/cast.h \
			$(srcdir)/src/Win32/include/openssl/comp.h \
			$(srcdir)/src/Win32/include/openssl/conf.h \
			$(srcdir)/src/Win32/include/openssl/conf_api.h \
			$(srcdir)/src/Win32/include/openssl/crypto.h \
			$(srcdir)/src/Win32/include/openssl/des.h \
			$(srcdir)/src/Win32/include/openssl/des_old.h \
			$(srcdir)/src/Win32/include/openssl/dh.h \
			$(srcdir)/src/Win32/include/openssl/dsa.h \
			$(srcdir)/src/Win32/include/openssl/dso.h \
			$(srcdir)/src/Win32/include/openssl/e_os2.h \
			$(srcdir)/src/Win32/include/openssl/ebcdic.h \
			$(srcdir)/src/Win32/include/openssl/ec.h \
			$(srcdir)/src/Win32/include/openssl/engine.h \
			$(srcdir)/src/Win32/include/openssl/err.h \
			$(srcdir)/src/Win32/include/openssl/evp.h \
			$(srcdir)/src/Win32/include/openssl/hmac.h \
			$(srcdir)/src/Win32/include/openssl/idea.h \
			$(srcdir)/src/Win32/include/openssl/krb5_asn.h \
			$(srcdir)/src/Win32/include/openssl/kssl.h \
			$(srcdir)/src/Win32/include/openssl/lhash.h \
			$(srcdir)/src/Win32/include/openssl/md2.h \
			$(srcdir)/src/Win32/include/openssl/md4.h \
			$(srcdir)/src/Win32/include/openssl/md5.h \
			$(srcdir)/src/Win32/include/openssl/mdc2.h \
			$(srcdir)/src/Win32/include/openssl/obj_mac.h \
			$(srcdir)/src/Win32/include/openssl/objects.h \
			$(srcdir)/src/Win32/include/openssl/ocsp.h \
			$(srcdir)/src/Win32/include/openssl/opensslconf.h \
			$(srcdir)/src/Win32/include/openssl/opensslv.h \
			$(srcdir)/src/Win32/include/openssl/ossl_typ.h \
			$(srcdir)/src/Win32/include/openssl/pem.h \
			$(srcdir)/src/Win32/include/openssl/pem2.h \
			$(srcdir)/src/Win32/include/openssl/pkcs12.h \
			$(srcdir)/src/Win32/include/openssl/pkcs7.h \
			$(srcdir)/src/Win32/include/openssl/rand.h \
			$(srcdir)/src/Win32/include/openssl/rc2.h \
			$(srcdir)/src/Win32/include/openssl/rc4.h \
			$(srcdir)/src/Win32/include/openssl/rc5.h \
			$(srcdir)/src/Win32/include/openssl/ripemd.h \
			$(srcdir)/src/Win32/include/openssl/rsa.h \
			$(srcdir)/src/Win32/include/openssl/safestack.h \
			$(srcdir)/src/Win32/include/openssl/sha.h \
			$(srcdir)/src/Win32/include/openssl/ssl.h \
			$(srcdir)/src/Win32/include/openssl/ssl2.h \
			$(srcdir)/src/Win32/include/openssl/ssl23.h \
			$(srcdir)/src/Win32/include/openssl/ssl3.h \
			$(srcdir)/src/Win32/include/openssl/stack.h \
			$(srcdir)/src/Win32/include/openssl/symhacks.h \
			$(srcdir)/src/Win32/include/openssl/tls1.h \
			$(srcdir)/src/Win32/include/openssl/tmdiff.h \
			$(srcdir)/src/Win32/include/openssl/txt_db.h \
			$(srcdir)/src/Win32/include/openssl/ui.h \
			$(srcdir)/src/Win32/include/openssl/ui_compat.h \
			$(srcdir)/src/Win32/include/openssl/x509.h \
			$(srcdir)/src/Win32/include/openssl/x509_vfy.h \
			$(srcdir)/src/Win32/include/openssl/x509v3.h

WIN32_LIB_SRC=$(srcdir)/src/Win32/lib/libeay32.lib \
			  $(srcdir)/src/Win32/lib/openssl.cnf \
			  $(srcdir)/src/Win32/lib/ssleay32.lib


WIN32_FILTER_SRC=$(srcdir)/src/Win32/PubCookieFilter.cpp \
			$(srcdir)/src/Win32/PubCookieFilter.def \
			$(srcdir)/src/Win32/PubCookieFilter.h  \
			$(srcdir)/src/Win32/PubCookieFilter.h.in  \
			$(srcdir)/src/Win32/PubCookieFilter.opt \
			$(srcdir)/src/Win32/PubCookieFilter.rc \
			$(srcdir)/src/Win32/PubCookieFilter.rc.in \
			$(srcdir)/src/Win32/PubCookieFilter.sln \
			$(srcdir)/src/Win32/PubCookieFilter.vcproj \
			$(srcdir)/src/Win32/resource.h \
			$(srcdir)/src/Win32/keys.h \
			$(srcdir)/src/Win32/keys.cpp \
			$(srcdir)/src/Win32/html.cpp \
			$(srcdir)/src/Win32/html.h


WIN32_MESSAGES_SRC=$(srcdir)/src/Win32/MSG00001.bin \
			$(srcdir)/src/Win32/pbc_messages.dsp \
			$(srcdir)/src/Win32/pbc_messages.h \
			$(srcdir)/src/Win32/pbc_messages.mc \
			$(srcdir)/src/Win32/pbc_messages.rc \
			$(srcdir)/src/Win32/pbc_messages.vcproj

WIN32_MISC_SRC=$(srcdir)/src/Win32/debug.c \
			$(srcdir)/src/Win32/debug.h \
			$(srcdir)/src/Win32/getopt.c \
			$(srcdir)/src/Win32/getopt.h 


WIN32_INSTALLER_SRC=$(srcdir)/src/Win32/installer/addfiltertometabaseenum.vbs \
			$(srcdir)/src/Win32/installer/addfiltertometabasemain.vbs \
			$(srcdir)/src/Win32/installer/find_webroot.vbs \
			$(srcdir)/src/Win32/installer/pubcookie.ism

WIN32_GUI_SRC=$(srcdir)/src/Win32/pbcgui/CPBC_PropSheet.cpp \
			$(srcdir)/src/Win32/pbcgui/CPBC_PropSheet.h \
			$(srcdir)/src/Win32/pbcgui/basesnap.Cpp \
			$(srcdir)/src/Win32/pbcgui/basesnap.Def \
			$(srcdir)/src/Win32/pbcgui/basesnap.h \
			$(srcdir)/src/Win32/pbcgui/extend.h \
			$(srcdir)/src/Win32/pbcgui/globals.h \
			$(srcdir)/src/Win32/pbcgui/gui_myconfig.cpp \
			$(srcdir)/src/Win32/pbcgui/gui_myconfig.h \
			$(srcdir)/src/Win32/pbcgui/pbcgui-directive.vcproj \
			$(srcdir)/src/Win32/pbcgui/pbcgui-server.vcproj \
			$(srcdir)/src/Win32/pbcgui/pbcgui.sln \
			$(srcdir)/src/Win32/pbcgui/pbcgui.suo \
			$(srcdir)/src/Win32/pbcgui/registry.Cpp \
			$(srcdir)/src/Win32/pbcgui/registry.h 

WIN32_GUI_SERVER_SRC=$(srcdir)/src/Win32/pbcgui/Server/GUIDs.h \
			$(srcdir)/src/Win32/pbcgui/Server/pbc_directives.h \
			$(srcdir)/src/Win32/pbcgui/Server/resource.Rc \
			$(srcdir)/src/Win32/pbcgui/Server/resource.h \
			$(srcdir)/src/Win32/pbcgui/Server/server.cpp


WIN32_GUI_DIRECTIVE_SRC=$(srcdir)/src/Win32/pbcgui/Directive/GUIDs.h \
			$(srcdir)/src/Win32/pbcgui/Directive/directive.Cpp \
			$(srcdir)/src/Win32/pbcgui/Directive/pbc_directives.h \
			$(srcdir)/src/Win32/pbcgui/Directive/resource.Rc \
			$(srcdir)/src/Win32/pbcgui/Directive/resource.h 

WIN32_KEYCLIENT_SRC=$(srcdir)/src/Win32/WebClient.c \
			$(srcdir)/src/Win32/WebClient.h \
			$(srcdir)/src/Win32/keyclient.opt \
			$(srcdir)/src/Win32/keyclient.sln \
			$(srcdir)/src/Win32/keyclient.vcproj \
			$(srcdir)/src/Win32/winkeyclient.c \
			$(srcdir)/src/Win32/winkeyclient.h

WIN32_SRC=$(WIN32_SSL_SRC) \
		  $(WIN32_LIB_SRC) \
		  $(WIN32_FILTER_SRC) \
		  $(WIN32_MESSAGES_SRC) \
		  $(WIN32_MISC_SRC) \
		  $(WIN32_GUI_SRC) \
		  $(WIN32_GUI_SERVER_SRC) \
		  $(WIN32_GUI_DIRECTIVE_SRC) \
		  $(WIN32_KEYCLIENT_SRC)

# Dist stuff

dist: a_ver l_ver
	$(MKDIR) $(DISTNAME)
	$(MKDIR) $(DISTNAME)/src
	$(MKDIR) $(DISTNAME)/doc
	$(MKDIR) $(DISTNAME)/cgic
	-$(RECURSIVE_CP) $(srcdir)/src/contrib $(DISTNAME)/src
	$(MKDIR) $(DISTNAME)/src/login_templates.generic
	$(MKDIR) $(DISTNAME)/src/login_templates.generic/media
	$(CP) $(LOGIN_TEMPLATES) $(DISTNAME)/src/login_templates.generic
	$(CP) $(LOGIN_MEDIA) $(DISTNAME)/src/login_templates.generic/media
	$(CP) $(DOCS) $(DISTNAME)/doc
	$(CP) $(CONFIGURE_FILES) $(DISTNAME)
	$(CP) $(SRC_CONFIGURE_FILES) $(DISTNAME)/src
	$(CP) $(TEST_SRC) $(UTIL_SRC) $(VERIFY_SRC) $(DISTNAME)/src
	$(CP) $(FLAVOR_SRC) $(INDEX_SRC) $(KEYMGT_SRC) $(LIB_SRC) $(DISTNAME)/src
	$(CP) $(MOD_SRC) $(MOD_HEAD) $(DISTNAME)/src
	$(CP) $(INDEX_HEAD) $(LIB_HEAD) $(DISTNAME)/src
	$(CP) $(CGIC_FILES) $(DISTNAME)/cgic
	$(CP) $(srcdir)/src/snprintf.c $(DISTNAME)/src
	$(CP) $(srcdir)/mod_pubcookie.exp $(DISTNAME)
	$(MKDIR) $(DISTNAME)/src/Win32
	$(MKDIR) $(DISTNAME)/src/Win32/include
	$(MKDIR) $(DISTNAME)/src/Win32/include/openssl
	$(MKDIR) $(DISTNAME)/src/Win32/lib
	$(MKDIR) $(DISTNAME)/src/Win32/pbcgui
	$(MKDIR) $(DISTNAME)/src/Win32/pbcgui/directive
	$(MKDIR) $(DISTNAME)/src/Win32/pbcgui/server
	$(MKDIR) $(DISTNAME)/src/Win32/installer
	$(CP) $(WIN32_SSL_SRC) $(DISTNAME)/src/Win32/include/openssl
	$(CP) $(WIN32_LIB_SRC) $(DISTNAME)/src/Win32/lib
	$(CP) $(WIN32_FILTER_SRC) $(DISTNAME)/src/Win32
	$(CP) $(WIN32_MISC_SRC) $(DISTNAME)/src/Win32
	$(CP) $(WIN32_KEYCLIENT_SRC) $(DISTNAME)/src/Win32
	$(CP) $(WIN32_MESSAGES_SRC) $(DISTNAME)/src/Win32
	$(CP) $(WIN32_GUI_SRC) $(DISTNAME)/src/Win32/pbcgui
	$(CP) $(WIN32_GUI_SERVER_SRC) $(DISTNAME)/src/Win32/pbcgui/server
	$(CP) $(WIN32_GUI_DIRECTIVE_SRC) $(DISTNAME)/src/Win32/pbcgui/directive
	$(CP) $(WIN32_INSTALLER_SRC) $(DISTNAME)/src/Win32/installer
	$(TAR) cf $(DISTNAME).tar $(DISTNAME)/
	$(GZIP) $(DISTNAME).tar
	$(RECURSIVE_FORCE_RM) ./$(DISTNAME)/

# vim: set noet:
