---
layout: page
title: "Custom Panel using React"
description: ""
date: 2016-07-29 12:00
sidebar: true
comments: false
sharing: true
footer: true
ha_category: User Interface
---

This is a [React](https://facebook.github.io/react/) implementation of [TodoMVC](http://todomvc.com/) but instead of checking off to do items, you are turning lights and switches on/off.

- It uses React to render the data.
- It hooks into Home Assistant JS which means updates pushed from the server are instantly rendered.
- It accesses properties made available from Polymer.
- It uses the user configuration for the component in the `configuration.yaml` file for rendering.
- It allows toggling the sidebar.

All you need is available as a [custom panel](https://github.com/home-assistant/home-assistant/tree/master/config/panels/react.html). Download the file and save it in `<config dir>/panels/` (you might have to create the directory if it doesn't exist).

Create a entry for the panel in your `configuration.yaml` file to enable it.

```yaml
panel_custom:
  - name: react
    sidebar_title: TodoMVC
    sidebar_icon: mdi:work
    url_path: todomvc
    config:
      title: hello
```

This video shows the example in action.

<div class='videoWrapper'>
<iframe width="560" height="315" src="https://www.youtube.com/embed/2200UutdXlo" frameborder="0" allowfullscreen></iframe>
</div>

