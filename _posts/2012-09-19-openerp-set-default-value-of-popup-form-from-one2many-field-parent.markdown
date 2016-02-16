---
layout: post
title: Openerp set default value of popup form from one2many field parent
date: 2012-09-19 15:51:06.000000000 +08:00
type: post
published: true
status: publish
categories:
- openerp
tags:
- one2many
- openerp
meta:
  _edit_last: '5225680'
author:
  login: paragasu
  email: paragasu@gmail.com
  display_name: paragasu
---

class definition (shop.py), please note the magic active_id

    class item(osv.osv):
    _name = "shop.item"
    _columns = {
      "item_id": fields.many2one("shop.cart", "Cart"),
    }

    _defaults = {
      "item_id": lambda self, cr, uid, c: c.get('item_id', False),
    }


    class cart(osv.osv):
    _name = "shop.cart"
    _columns = {
      "item_ids": one2many("shop.item", "item_id", "Items"),
    }

In the view definition for the one2many field (shop_view.xml)

    <field name="item_ids" domain="['item_id', '=', active_id]" context="{'item_id': active_id}">

