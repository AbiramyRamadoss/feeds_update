include $(TOPDIR)/rules.mk

PKG_NAME:=hello_feeds
PKG_VERSION:=1.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/AbiramyRamadoss/myscr.git
PKG_SOURCE_VERSION:=c39a47117bf0b5c71ea7f42ad29b498068f1f9c1
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_SOURCE_VERSION)
PKG_SOURCE:=$(PKG_SOURCE_SUBDIR).tar.xz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)

include $(INCLUDE_DIR)/package.mk

define Package/hello_feeds
	SECTION:=zilogic
	CATEGORY:=test
	TITLE:=hello_world_feeds
endef

define Package/hello_feeds/description
	Hello World Feeds.
endef

define Build/Compile
	$(MAKE) CC=$(TARGET_CC) -C $(PKG_BUILD_DIR)/
endef

define Package/hello_feeds/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/hello $(1)/usr/bin/
endef

$(eval $(call BuildPackage,hello_feeds))
