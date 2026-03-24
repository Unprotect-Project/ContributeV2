rule xor_detection
{
    strings:
        $xor1 = { 31 d2 f7 e2 89 c2 }
        $xor2 = { 31 c9 f7 f9 99 c0 }
        $xor3 = { 31 f6 f7 e6 99 d0 }

    condition:
        any of them
}