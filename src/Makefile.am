lib_LTLIBRARIES = libXt.la

BUILT_SOURCES = $(BUILT_FILES)
CLEANFILES = $(BUILT_SOURCES)

AM_CFLAGS = $(XT_CFLAGS) $(X11_CFLAGS)

INCLUDES = -I$(top_srcdir)/include/ -I$(top_srcdir)/include/X11 \
	   -I$(top_builddir)/include -I$(top_builddir)/include/X11

nodist_libXt_la_SOURCES = StringDefs.c

libXt_la_SOURCES = \
	ActionHook.c \
	Alloc.c \
	ArgList.c \
	Callback.c \
	ClickTime.c \
	Composite.c \
	Constraint.c \
	Convert.c \
	Converters.c \
	Core.c \
	Create.c \
	Destroy.c \
	Display.c \
	Error.c \
	Event.c \
	EventUtil.c \
	Functions.c \
	GCManager.c \
	Geometry.c \
	GetActKey.c \
	GetResList.c \
	GetValues.c \
	HookObj.c \
	Hooks.c \
	Initialize.c \
	Intrinsic.c \
	Keyboard.c \
	Manage.c \
	NextEvent.c \
	Object.c \
	PassivGrab.c \
	Pointer.c \
	Popup.c \
	PopupCB.c \
	RectObj.c \
	ResConfig.c \
	Resources.c \
	Selection.c \
	SetSens.c \
	SetValues.c \
	SetWMCW.c \
	Shell.c \
	TMaction.c \
	TMgrab.c \
	TMkey.c \
	TMparse.c \
	TMprint.c \
	TMstate.c \
	Threads.c \
	VarCreate.c \
	VarGet.c \
	Varargs.c \
	Vendor.c \
	sharedlib.c

DISTCLEANFILES = StringDefs.c

libXt_la_LIBADD = @XT_LIBS@

libXt_la_LDFLAGS = -version-number 6:0:0 -no-undefined
