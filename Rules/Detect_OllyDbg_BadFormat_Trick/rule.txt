rule Detect_OllyDBG_BadFormatTrick: AntiDebug {
    meta: 
        description = "Detect bad format not handled by Ollydbg"
        author = "Unprotect"
        comment = "Experimental rule"
    strings:
        $1 = "%s%s.exe" fullword ascii
    condition:   
       $1
}