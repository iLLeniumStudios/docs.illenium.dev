---
title: Theme Configuration
---

fivem-appearance comes with 3 themes, `default`, `qb-core`, and `project-sloth` and `qb-core` is set as the default one.

### Switch between themes

Change `currentTheme` to the theme `id`. You can choose between `qb-core`, `default`, and `project-sloth`.

### Creating custom themes

- Copy an existing theme based on which you want to create a new one
- Change the `id` to something unique
- Change the parameters of the theme accordingly

### Theme parameters

You can customize every theme using the parameters defined in `theme.json`. Following table explains a little bit about what each parameter can do

| Parameter                  | Description                                                   |
|:----------------------------|:---------------------------------------------------------------|
| id                         | Unique ID for the theme                                       |
| borderRadius               | How round do you want the corners of the elements to be       |
| fontColor                  | Main color of the text                                        |
| fontColorHover             | Color of the text on hover                                    |
| fontColorSelected          | Color of the text when it is selected                         |
| fontFamily                 | Font of the text                                              |
| primaryBackground          | Main background color for the elements                        |
| primaryBackgroundSelected  | Main background color for the elements when they are selected |
| secondaryBackground        | Secondary background color                                    |
| scaleOnHover               | Increase the size of the elements on hover                    |
| sectionFontWeight          | Font weight for the section headings text                     |
| smoothBackgroundTransition | Enable to fade in to the background color during hover        |

!!!important
    After creating the custom theme, make sure to change `currentTheme` to the `id` of the new theme. You can ofcourse modify the existing themes as well if you want, but it is recommended to create your own so that you can switch between the defaults and the custom one whenever needed.
