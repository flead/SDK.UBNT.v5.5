#
# Copyright (C) 2006 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
# $Id: Makefile 9304 2007-10-14 04:32:56Z blogic $

include $(TOPDIR)/rules.mk

PKG_NAME:=iftop
PKG_VERSION:=0.17
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=http://www.ex-parrot.com/~pdw/iftop/download
PKG_MD5SUM:=062bc8fb3856580319857326e0b8752d

include $(INCLUDE_DIR)/package.mk

define Package/iftop
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+libpcap +libncurses +libpthread
  TITLE:=display bandwith usage on an interface
  URL:=http://www.ex-parrot.com/~pdw/iftop/
endef

define Package/iftop/description
	iftop does for network usage what top(1) does for CPU usage. It 
	listens to network traffic on a named interface and displays a 
	table of current bandwidth usage by pairs of hosts. Handy for 
	answering the question 'why is our ADSL link so slow?'.
endef

define Package/iftop/install	
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/iftop $(1)/usr/bin/
endef

$(eval $(call BuildPackage,iftop))
