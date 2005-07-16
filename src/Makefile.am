lib_LTLIBRARIES = libXt.la

BUILT_SOURCES = $(BUILT_FILES)
CLEANFILES = $(BUILT_SOURCES)

AM_CFLAGS = $(XT_CFLAGS) $(X11_CFLAGS)

INCLUDES = -I$(top_srcdir)/include/ -I$(top_srcdir)/include/X11

nodist_libXt_la_SOURCES = StringDefs.c

libXt_la_SOURCES = \
	ActionHook.c \
	Alloc.c \
	ArgList.c \
	Callback.c \
	CallbackI.h \
	ClickTime.c \
	Composite.c \
	Constraint.c \
	Convert.c \
	ConvertI.h \
	Converters.c \
	Core.c \
	Create.c \
	CreateI.h \
	Destroy.c \
	Display.c \
	Error.c \
	Event.c \
	EventI.h \
	EventUtil.c \
	Functions.c \
	GCManager.c \
	Geometry.c \
	GetActKey.c \
	GetResList.c \
	GetValues.c \
	HookObj.c \
	HookObjI.h \
	Hooks.c \
	InitialI.h \
	Initialize.c \
	Intrinsic.c \
	IntrinsicI.h \
	Keyboard.c \
	Manage.c \
	NextEvent.c \
	Object.c \
	PassivGraI.h \
	PassivGrab.c \
	Pointer.c \
	Popup.c \
	PopupCB.c \
	RectObj.c \
	ResConfig.c \
	ResConfigP.h \
	ResourceI.h \
	Resources.c \
	Selection.c \
	SelectionI.h \
	SetSens.c \
	SetValues.c \
	SetWMCW.c \
	Shell.c \
	ShellI.h \
	TMaction.c \
	TMgrab.c \
	TMkey.c \
	TMparse.c \
	TMprint.c \
	TMstate.c \
	Threads.c \
	ThreadsI.h \
	TranslateI.h \
	VarCreate.c \
	VarGet.c \
	Varargs.c \
	VarargsI.h \
	Vendor.c \
	Xtos.h \
	sharedlib.c

libXt_la_LIBADD = @XT_LIBS@

libXt_la_LDFLAGS = -version-number 6:0:0 -no-undefined
