include $(TOPDIR)/rules.mk

PECL_NAME:=phalcon
PECL_LONGNAME:=PHP5 phalcon Extension

PKG_NAME:=php5-pecl-$(PECL_NAME)
PKG_VERSION:=3.1.2
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/phalcon/cphalcon.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=47b23351bf16b8fcece3424e9b2371d89773c753
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_BUILD_DEPENDS:=php5

#PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php5/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php5/$(PECL_NAME)-$(PKG_VERSION)/ext
#PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php5/$(PECL_NAME)-$(PKG_VERSION)/build/php5/32bits
#PKG_BUILD_PARALLEL:=1

PKG_LICENSE:=PHPv3.01
PKG_LICENSE_FILES:=

PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include ../php5/pecl.mk

define Package/php5-pecl/Default
CONFIGURE_ARGS+=  --enable-phalcon 
endef

$(eval $(call PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
