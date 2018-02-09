**Serial Port Emulation. Learn how to use Virtual Port Emulator.**
==================================================================

Employing virtual devices to simulate the behavior of their physical counterparts has long been a widely accepted method of developing, testing and debugging software.

**[Serial port emulation](https://www.eltima.com/virtual-serial-port-emulation.html)** is used by developers of complex serial communication systems. Programmers can use a variety of software tools that provide operating systems (primarily Windows OS) with virtual serial ports. These software solutions allow testing and monitoring of serial port communications between RS232 and [RS484 interfaces](https://www.eltima.com/article/rs485-communication-guide/).

Even applications designed to work with hardware COM ports that are resident on client computers can be tested without connecting to physical serial ports, Dedicated software tools enable the creation of pairs of virtual COM ports that communicate by way of a **[virtual null-modem cable](https://www.eltima.com/products/virtual-null-modem/)**. You can also develop a serial port emulator yourself to simplify the testing and monitoring of data traffic between your program and a physical COM port.

**Serial port emulation: main principles**
------------------------------------------

1. Programmers can use multiple virtual serial ports, allowing them to diagnose and debug software on systems containing no physical serial ports.

**As an example**, consider that a programmer developing and debugging an application for serial communication will usually need at least two physical serial ports. Currently, most computers provide at most one serial port, forcing a developer to either use two machines or obtain a PCI card containing a COM port. By using the serial port emulator the programmer can now create multiple virtual COM ports on one computer, allowing any serial communication program to be developed on any computer that can run the emulator.

2. By emulating COM ports, developers no longer need to use complex software to control interprocess communication and the sharing of physical resources. The speed of data transmission is not dependent on the physical COM port but relies on your system specifications as traffic moves between the virtual ports. 

3. Virtual serial ports can replicate all the parameters of physical serial ports and provides strict baudrate emulation. 

**[Virtual COM Port Driver](https://www.eltima.com/virtual-com-port/) by Eltima Software** is a powerful serial port emulator that offers advanced functionality built on a simple, user-friendly interface. All recent versions of the Windows operating system are supported by VSPD. The tool is even more stable when run on Windows 10 as it is digitally signed with WHQL. These are just a few of the many reasons that make Virtual Serial Port Driver one of the best and effective serial port emulate tools available.

**Serial port simulation with different programming languages**
---------------------------------------------------------------

To simplify working with files and devices, standard options such as CreatePair, DeletPair, SetStrictBaudrate and others are fully supported by VSPD. Below are some examples of how you can take advantage of Virtual Serial Port Driver with some popular programming languages.

**C/C++**
     
Load the DLL file dynamically and then choose and call your desired functions to effectively use virtual port emulator. Here’s how it looks in Visual C++ :

    typedef bool (stdcall *CreatePairFn)(char *Port1, char *Port2);
    typedef bool (stdcall *DeletePairFn)(char *Port);
    typedef bool (stdcall *DeleteAllFn)(void);
    typedef bool (stdcall *SetStrictBaudrateFn) (char *Port, bool StrictBaudrate);
    typedef bool (stdcall *SetBreakFn) (char *Port, bool bBreak);
    typedef bool (stdcall *QueryBusFn) (void* InBuffer, long sizeInBuffer, void* OutBuffer, long sizeOutBuffer);
    typedef bool (stdcall *SetWiringFn) (char *Port, void *Buffer, long sizeBuffer);
    typedef bool (stdcall *SetAccessListFn) (char *Port, void *Buffer, long sizeBuffer);
 
    typedef bool (stdcall *CreatePairExFn)(char *Port1, char *Port2, char * UserSession);
    typedef bool (stdcall *CreatePairWFn)(WCHAR *Port1, WCHAR *Port2);
    typedef bool (stdcall *CreatePairExWFn)(WCHAR *Port1, WCHAR *Port2, WCHAR * UserSession);
    typedef bool (stdcall *DeletePairWFn)(WCHAR *Port);
    typedef bool (stdcall *SetStrictBaudrateWFn) (WCHAR *Port, bool StrictBaudrate);
    typedef bool (stdcall *SetBreakWFn) (WCHAR *Port, bool bBreak);
    typedef bool (stdcall *SetWiringWFn) (WCHAR *Port, void *Buffer, long sizeBuffer);
    typedef bool (stdcall *SetAccessListWFn) (WCHAR *Port, void *Buffer, long sizeBuffer);
    typedef bool (stdcall *DeletePairExFn)(char *Port, char * UserSession);
    typedef bool (stdcall *DeletePairExWFn)(WCHAR *Port, WCHAR * UserSession);
 
    typedef bool (stdcall *GetUserSessionFn)(char *Session, int &iSize);
    typedef bool (stdcall *GetUserSessionWFn)(WCHAR *Session, int &iSize);
 
    typedef bool (stdcall *SetStrictBaudrateExWFn) (WCHAR *Port, WCHAR * UserSession, bool StrictBaudrate);
    typedef bool (stdcall *SetStrictBaudrateExFn) (char *Port, char * UserSession, bool StrictBaudrate);
    typedef bool (stdcall *SetBreakExWFn) (WCHAR *Port, WCHAR * UserSession, bool bBreak);
    typedef bool (stdcall *SetBreakExFn) (char *Port, char * UserSession, bool bBreak);
    typedef bool (stdcall *SetAccessListExWFn) (WCHAR *Port, WCHAR * WCHAR, void *Buffer, long sizeBuffer);
    typedef bool (stdcall *SetAccessListExFn) (char *Port, char * WCHAR, void *Buffer, long sizeBuffer);
    bool CreateVSPair(char *Port1, char *Port2) {
    OSVERSIONINFO VersionInfo;
    HINSTANCE libInst;
    libInst = LoadLibrary(VSPDCTL.DLL);
    if (!libInst)
       return false; /* Couldn't load library */
    /* Substitute the typedefs above for functions other than CreatePairFn */
    CreatePairFn CreatePair=(CreatePairFn)GetProcAddress(libInst, â€œCreatePairâ€);
    if (CreatePair==0) return false; /* Couldn`t find function */
    returnvalue=CreatePair(Port1, Port2); /* For example, Port1 = â€œCOM5â€³ and Port2 = â€œCOM6â€³ */
    FreeLibrary(libInst);
    return returnvalue;
    };
 
**Visual Basic**

With Visual Basic, you need to paste these lines into your source file to access the functionality of VSPD:

    Declare Function CreatePair Lib "VSPDCTL.DLL" (ByVal Port1$, ByVal Port2$) As Boolean
    Declare Function DeletePair Lib "VSPDCTL.DLL" (ByVal Port$) As Boolean
    Declare Function DeleteAll Lib "VSPDCTL.DLL" () As Boolean
    Declare Function SetStrictBaudrateName Lib "VSPDCTL.DLL" (ByVal Port$, ByVal StrictBaudrate As Boolean) As Boolean
    Declare Function SetStrictBaudrateHandle Lib "VSPDCTL.DLL" (ByVal Handle As Long, ByVal StrictBaudrate As Boolean) As Boolean
    Declare Function CreatePair Lib "VSPDCTL.DLL" (ByVal Port1$, ByVal Port2$) As Boolean
    Declare Function DeletePair Lib "VSPDCTL.DLL" (ByVal Port$) As Boolean
    Declare Function DeleteAll Lib "VSPDCTL.DLL" () As Boolean
    Declare Function SetStrictBaudrate Lib "VSPDCTL.DLL" (ByVal Port$, ByVal StrictBaudrate As Boolean) As Boolean
    Declare Function SetBreak Lib "VSPDCTL.DLL" (ByVal Port$, ByVal bBreak As Boolean) As Boolean
    Declare Function QueryBus Lib "VSPDCTL.DLL" (ByVal InBuffer As String, sizeInBuffer As Long, ByVal OutBuffer As String, sizeOutBuffer As Long) As Boolean
    Declare Function SetWiring Lib "VSPDCTL.DLL" (ByVal Port1$, ByVal Buffer As String, sizeBuffer As Long) As Boolean
    
With the VSPDCTL.DLL in your application’s directory, the functions can be called directly.

**Delphi**

Here are the function declarations for Delphi:

    Function CreatePair(Port1, Port2 : PChar) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function DeletePair(Port : PChar) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function DeleteAll : Boolean; stdcall; external "VSPDCTL.DLL";
    Function SetStrictBaudrateName(Port: PChar, StrictBaudrate: Boolean) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function SetStrictBaudrateHandle(hPort: THandle, StrictBaudrate: Boolean) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function CreatePair(Port1, Port2 : PChar) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function DeletePair(Port : PChar) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function DeleteAll : Boolean; stdcall; external "VSPDCTL.DLL";
    Function SetStrictBaudrate(Port: PChar, StrictBaudrate: Boolean) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function SetBreak (Port: PChar, bBreak: Boolean) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function QueryBus (InBuffer: Pointer, sizeInBuffer: Integer, OutBuffer: Pointer, sizeOutBuffer: Integer) : Boolean; stdcall; external "VSPDCTL.DLL";
    Function SetWiring (Port: PChar Buffer: Pointer, sizeBuffer: Integer) : Boolean; stdcall; external "VSPDCTL.DLL";

ArmAccess can be loaded statically or dynamically. For dynamic loading, use this sample code:

    Function CreatePairFn(PortName1, PortName2 : String) : Boolean;
    Type TCreatePair = function(Port1, Port2 : PChar) : Boolean; stdcall;
    Var Handle : THandle;
    CreatePair : TCreatePair;
    Begin
    CreatePairFn := False;
    Handle := LoadLibrary("VSPDCTL.DLL");
    If (Handle <> 0) Then
    Begin
    @CreatePair:=GetProcAddress(Handle, "CreatePair");
    If (CreatePair <> Nil) Then
    CreatePairFn := CreatePair(PChar(PortName1), PChar(PortName2));
    FreeLibrary(Handle);
    End;
    End;














