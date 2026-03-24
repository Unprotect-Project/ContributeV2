rule Detect_Interrupt: AntiDebug {
    meta: 
        description = "Detect Interrupt instruction"
        author = "Unprotect"
        comment = "Experimental rule / the rule can be slow to use"
    strings:
        $int3 = { CC }
        $intCD = { CD }
        $int03 = { 03 }
        $int2D = { 2D }
        $ICE = { F1 }
    condition:   
       uint16(0) == 0x5A4D and filesize < 1000KB and any of them
}