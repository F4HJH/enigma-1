# ENIGMA
This is a small application written in python which simulates both the M3 and M4, 3 and 4 rotor variants of the Enigma machine which was utilised by German forces during WWII to encode information.

Included are two scripts for a quick demo of each: `enigmaM3_test.py` and `enigmaM4_test.py` which have preset keys and rotor selection.

## Custom Machine
To create a new instance of Enigma the default can be used which is an M3 instance with pre-selected rotor arrangement and reflector choice, or all settings can be chosen by the user. Note as with the machine itself, one of the 8 numbered rotor types may only be selected once:
```
my_rotor_list = [1,4,6,3]     # 3 or 4 of 1,2,3,4,5,6,7,8
my_reflector  = 'B'           # 'B' or 'C'
machine_type  = 'M4'          # 'M3' or 'M4' (should match rotor list)
debug_level   = 'ERROR'       # 'ERROR', 'INFO', 'DEBUG' (see python 'logging' module documentation)

enigma = enigma.Enigma( rotor_list     = my_rotor_list ,
                        user_reflector = my_reflector  ,
                        enigma_type    = machine_type  ,
                        debug          = debug_level)

enigma.setkey('NERO')
enigma.type_phrase('NOBODYEXPECTSTHESPANISHINQUISITION')
```
