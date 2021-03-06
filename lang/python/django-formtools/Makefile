#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=django-formtools
PKG_VERSION:=2.1
PKG_RELEASE:=7

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=7703793f1675aa6e871f9fed147e8563816d7a5b9affdc5e3459899596217f7c

PKG_MAINTAINER:=Eneas U de Queiroz <cotequeiroz@gmail.com>
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/django-formtools/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=High-level abstractions for Django forms
  URL:=https://django-formtools.readthedocs.io
endef

define Package/python3-django-formtools
$(call Package/django-formtools/Default)
  DEPENDS:= \
	+PACKAGE_python3-django-formtools:python3 \
	+PACKAGE_python3-django-formtools:python3-django1
  VARIANT:=python3
endef

define Package/python3-django-formtools/description
  Django "formtools" is a set of high-level abstractions for Django forms.
  Currently for form previews and multi-step forms.
.
(Variant for Python3)
endef

$(eval $(call Py3Package,python3-django-formtools))
$(eval $(call BuildPackage,python3-django-formtools))
$(eval $(call BuildPackage,python3-django-formtools-src))
