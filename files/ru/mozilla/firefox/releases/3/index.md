---
title: Firefox 3 для разработчиков
slug: Mozilla/Firefox/Releases/3
---

Если вы разработчик и хотите познакомится со всеми возможностями Firefox 3 вы пришли по адресу. В этой статье представлен список новых статей, в которых рассказывается о новых возможностях Firefox 3. В статьях не будут представлены сведения о незначительных изменениях, однако они помогут вам познакомится с существенными обновлениями.

### Новые возможности для разработчиков в Firefox 3

#### Для веб-мастеров и разработчиков приложений

- [Обновление веб-приложений для Firefox 3](/ru/%D0%9E%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5_%D0%B2%D0%B5%D0%B1-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B9_%D0%B4%D0%BB%D1%8F_Firefox_3)
  - : Предоставляет информацию об изменениях которые вам возможно нужно внести, чтобы получить выгоду от новых возможностей Firefox 3.

- [Online и offline события](/en/Online_%D0%B8_offline_%D1%81%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D1%8F)
  - : Firefox 3 поддерживает WHATWG online и offline события, которые позволяют приложениям и расширениям определять есть ли активное Интернет соединение, и так же позволяет определять когда появляется и пропадает соединение.

- [Веб-ориентированные обработчики протоколов](/ru/%D0%92%D0%B5%D0%B1-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5_%D0%BE%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA%D0%B8_%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%D0%BE%D0%B2)
  - : Теперь вы можете регистрировать веб-приложения как обработчик протокола используя метод `navigator.registerProtocolHandler()`.

- [Рисование текста с использованием canvas](/ru/%D0%A0%D0%B8%D1%81%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5_%D1%82%D0%B5%D0%BA%D1%81%D1%82%D0%B0_%D1%81_%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%D0%BC_canvas)
  - : Теперь вы можете рисовать текст с использованием нестандартизированного API canvas поддерживаемого Firefox 3.

- [Поддержка преобразований для canvas](/en-US/Canvas_tutorial/Transformations#transforms)
  - : Firefox now supports the `transform()` and `setTransform()` methods on canvases.

- [Using microformats](/en-US/Using_microformats)
  - : Firefox now has APIs for working with microformats.

- [Drag and drop events](/en-US/Drag_and_drop_events)
  - : Firefox 3 supports new events that are sent to the source node for a drag operation when the drag begins and ends.

- [Focus management in HTML](/en-US/Focus_management_in_HTML)
  - : The new HTML 5 `activeElement` and `hasFocus` attributes are supported.

- [Offline resources in Firefox](/en-US/Offline_resources_in_Firefox)
  - : Firefox now lets web applications request that resources be cached to allow the application to be used while offline.

- [CSS improvements in Firefox 3](/en-US/CSS_improvements_in_Firefox_3)
  - : Firefox 3 features a number of improvements in its CSS support.

- [DOM improvements in Firefox 3](/en-US/DOM_improvements_in_Firefox_3)
  - : Firefox 3 offers a number of new features in Firefox 3's DOM implementation, including support for several Internet Explorer extensions to the DOM.

- [JavaScript 1.8 support](/en-US/New_in_JavaScript_1.8)
  - : Firefox 3 offers JavaScript 1.8.

- [EXSLT support](/en-US/EXSLT)
  - : Firefox 3 provides support for a substantial subset of the [EXSLT](/en-US/EXSLT) extensions to [XSLT](/en-US/XSLT).

- [SVG improvements in Firefox 3](/en-US/SVG_improvements_in_Firefox_3)
  - : SVG support in Firefox 3 has been upgraded significantly, with support for over two dozen new filters, several new elements and attributes, and other improvements.

- [Animated PNG graphics](/en-US/Animated_PNG_graphics)
  - : Firefox 3 supports the animated PNG (APNG) image format.

#### For XUL and extension developers

##### Notable changes and improvements

- [Updating extensions for Firefox 3](/en-US/Updating_extensions_for_Firefox_3)
  - : Provides a guide to the things you'll need to do to update your extension to work with Firefox 3.

- [XUL improvements in Firefox 3](/en-US/XUL_improvements_in_Firefox_3)
  - : Firefox 3 offers a number of new XUL elements, including new sliding scales, the date and time pickers, and spin buttons.

- [Templates in Firefox 3](/en-US/Templates_in_Firefox_3)
  - : Templates have been significantly improved in Firefox 3. The key improvement allows the use of custom query processors to allow data sources other than RDF to be used.

- [Securing updates](/en-US/Extension_Versioning,_Update_and_Compatibility#securing_updates)
  - : In order to provide a more secure add-on upgrade path for users, add-ons are now required to provide a secure method for obtaining updates before they can be installed. Add-ons hosted at [AMO](https://addons.mozilla.org) automatically provide this. Any add-ons installed that do not provide a secure update method when the user upgrades to Firefox 3 will be automatically disabled. Firefox will however continue to check for updates to the extension over the insecure path and attempt to install any update offered (installation will fail if the update also fails to provide a secure update method).

- [Places migration guide](/en-US/Places_migration_guide)
  - : An article about how to update an existing extension to use the Places API.

- [Download Manager improvements in Firefox 3](/en-US/Download_Manager_improvements_in_Firefox_3)
  - : The Firefox 3 Download Manager features new and improved APIs, including support for multiple progress listeners.

- [Using nsILoginManager](/en-US/Using_nsILoginManager)
  - : The Password Manager has been replaced by the new Login Manager.

- [Embedding XBL bindings](/en-US/XBL/XBL_1.0_Reference/Elements#binding)
  - : You can now use the `data:` URL scheme from chrome code to embed XBL bindings directly instead of having them in separate XML files.

- [Localizing extension descriptions](/en-US/Localizing_extension_descriptions)
  - : Firefox 3 offers a new method for localizing add-on metadata. This lets the localized details be available as soon as the add-on has been downloaded, as well as when the add-on is disabled.

- [Localization and Plurals](/en-US/Localization_and_Plurals)
  - : Firefox 3 adds the new PluralForm module, which provides tools to aid in correctly pluralizing words in multiple localizations.

- [Theme changes in Firefox 3](/en-US/Theme_changes_in_Firefox_3)
  - : Notes and information of use to people who want to create themes for Firefox 3.

##### New components and functionality

- [FUEL Library](/en-US/FUEL)
  - : FUEL is about making it easier for extension developers to be productive, by minimizing some of the XPCOM formality and adding some "modern" JavaScript ideas.

- [Places](/en-US/Places)
  - : The history and bookmarks APIs have been completely replaced by the new [Places](/en-US/Places) API.

- [Idle service](/en-US/nsIIdleService)
  - : Firefox 3 offers the new `nsIIdleService` interface, which lets extensions determine how long it's been since the user last pressed a key or moved their mouse.

- [ZIP writer](/en-US/nsIZipWriter)
  - : The new `nsIZipWriter` interface lets extensions create ZIP archives.

- [Full page zoom](/en-US/Full_page_zoom)
  - : Firefox 3 improves the user experience by offering full page zoom in addition to text-only zoom.

- [Interfacing with the XPCOM cycle collector](/en-US/Interfacing_with_the_XPCOM_cycle_collector)
  - : XPCOM code can now take advantage of the cycle collector, which helps ensure that unused memory gets released instead of leaking.

- [The Thread Manager](/en-US/The_Thread_Manager)
  - : Firefox 3 provides the new `nsIThreadManager` interface, along with new interfaces for threads and thread events, which provides a convenient way to create and manage threads in your code.

- [JavaScript modules](/en-US/JavaScript_modules)
  - : Firefox 3 now offers a new shared code module mechanism that lets you easily create modules in JavaScript that can be loaded by extensions and applications for use, much like shared libraries.

- [The `nsIJSON` interface](/en-US/nsIJSON)
  - : Firefox 3 offers the new `nsIJSON` interface, which offers high-performance encoding and decoding of [JSON](/en-US/JSON) strings.

- [The nsIParentalControlsService interface](/en-US/nsIParentalControlsService)
  - : Firefox 3 now supports the Microsoft Windows Vista parental controls feature, and allows code to interact with it.

- [Using content preferences](/en-US/Using_content_preferences)
  - : Firefox 3 includes a new service for getting and setting arbitrary site-specific preferences that extensions as well as core code can use to keep track of their users' preferences for individual sites.

- [Plug-in Monitoring](/en-US/Monitoring_plugins)
  - : A new component of the plugin system is now available to measure how long it takes plugins (e.g., Macromedia Flash) to execute their calls.

##### Fixed bugs

- [Notable bugs fixed in Firefox 3](/en-US/Notable_bugs_fixed_in_Firefox_3)
  - : This article provides information about bugs that have been fixed in Firefox 3.

### New features for end users

#### User experience

- **Easier password management.** An information bar at the top of the browser window now appears to allow you to save passwords after a successful login.
- **Simplified add-on installation.** You can now install extensions from third-party download sites in fewer clicks, thanks to the removal of the add-on download site whitelist.
- **New Download Manager.** The download manager makes it easier to locate your downloaded files.
- **Resumable downloads.** You can now resume downloads after restarting the browser or resetting your network connection.
- **Full page zoom.** From the View menu and using keyboard shortcuts, you can now zoom in and out on the content of entire pages — this scales not just the text but the layout and images as well.
- **Tab scrolling and quickmenu.** Tabs are easier to locate with the new tab scrolling and tab quickmenu features.
- **Save what you were doing.** Firefox 3 prompts you to see if you'd like to save your current tabs when you exit Firefox.
- **Optimized Open in Tabs behavior.** Opening a folder of bookmarks in tabs now appends the new tabs instead of replacing the existing ones.
- **Easier to resize location and search bars.** You can now easily resize the location and search bars using a simple resize handle between them.
- **Text selection improvements.** You can now select multiple ranges of text using the Control (Command on Macintosh) key. Double-clicking and dragging now selects in "word-by-word" mode. Triple-clicking selects an entire paragraph.
- **Find toolbar.** The Find toolbar now opens with the current selection.
- **Plugin management.** Users can now disable individual plugins in the Add-on Manager.
- **Integration with Windows Vista.** Firefox's menus now display using Vista's native theme.
- **Integration with Mac OS X.** Firefox now supports [Growl](http://growl.info/) for notifications of completed downloads and available updates.
- **Star button.** The new star button in the location bar lets you quickly add a new bookmark with a single click. A second click lets you file and tag your new bookmark.
- **Tags.** You can now associate keywords with your bookmarks to easily sort them by topic.
- **Location bar and auto-complete.** Type the title or tag of a page in the location bar to quickly find the site you were looking for in your history and bookmarks. Favicons, bookmark, and tag indicators help you see where the results are coming from.
- **Smart Bookmarks folder.** Firefox's new Smart Bookmarks folder offers quick access to your recently bookmarked and tagged places, as well as pages you visit frequently.
- **Bookmarks and History Organizer.** The new unified bookmarks and history organizer lets you easily search your history and bookmarks with multiple views and smart folders for saving your frequent searches.
- **Web-based protocol handlers.** Web applications, such as your favorite web mail provider, can now be used instead of desktop applications for handling `mailto:` links from other sites. Similar support is provided for other protocols as well. (Note that web applications do have to register themselves with Firefox before this will work.)
- **Easy to use Download Actions.** A new Applications preferences pane provides an improved user interface for configuring handlers for various file types and protocol schemes.
- **Improved look and feel.** Graphics and font handling have been improved to make web sites look better on your screen, including sharper text rendering and better support for fonts with ligatures and complex scripts. In addition, Mac and Linux (Gnome) users will find that Firefox feels more like a native application for their platform than ever, with a new, native, look and feel.
- **Color management support.** By setting the `gfx.color_management.enabled` preference in `about:config`, you can ask Firefox to use the color profiles embedded in images to adjust the colors to match your computer's display.
- **Offline support.** Web applications can take advantage of new features to support being used even when you don't have an Internet connection.

#### Security and privacy

- **One-click site information.** Want to know more about the site you're visiting? Click the site's icon in the location bar to see who owns it. Identify information is prominently displayed and easier than ever to understand.
- **Malware protection.** Firefox 3 warns you if you arrive at a web site that is known to install viruses, spyware, trojans, or other dangerous software (known as malware). You can see what the warning looks like by [clicking here](https://www.mozilla.com/firefox/its-an-attack.html).
- **Web forgery protection enhanced.** Now when you visit a page that's suspected of being a forgery, you're shown a special page instead of the contents of the page with a warning. [Click here](https://www.mozilla.com/firefox/its-a-trap.html) to see what it looks like.
- **Easier to understand SSL errors.** The errors presented when an invalid SSL certificate is encountered have been clarified to make it easier to understand what the problem is.
- **Out-of-date add-on protection.** Firefox 3 now automatically checks add-on and plugin versions and disables older, insecure versions.
- **Secure add-on updates.** Add-on update security has been improved by disallowing add-ons that use an insecure update mechanism.
- **Anti-virus integration.** Firefox 3 now informs anti-virus software when executable files are downloaded.
- **Windows Vista parental controls support.** Firefox 3 supports the Vista system-wide parental control setting for disabling file downloads.

#### Performance

- **Reliability.** Firefox 3 now stores bookmarks, history, cookies, and preferences in a transactionally secure database format. This means your data is protected against loss even if your system crashes.
- **Speed.** Firefox 3 has gotten a performance boost by completely replacing the part of the software that handles drawing to your screen, as well as to how page layout work is handled.
- **Memory use reduced.** Firefox 3 is more memory efficient than ever, with over 300 memory "leak" bugs fixed and new features to help automatically locate and dispose of leaked memory blocks.

## Смотрите также

- [Updating extensions for Firefox 3](/en-US/Updating_extensions_for_Firefox_3)
- [Updating web applications for Firefox 3](/en-US/Updating_web_applications_for_Firefox_3)
- [Firefox 2 for developers](/en-US/Firefox_2_for_developers)
- [Firefox 1.5 for developers](/en-US/Firefox_1.5_for_developers)
