import math
#formula used to solve this
#logbaseX {I(p)/sqrt(n)} x X^m = M
"""
ex of an input will be this below but without spaces or new lines
- - - -
- - - -
- m - -
- - - p
ex: ---------m-----p
"""
"""
----
----
-m--
---p
"""
def ini():
    #ask first input
    first_input = input()
    
    #insert them into to a list
    list = []
    list.append(first_input)
    
    
    #create second list to furthr down list's list with a loop
    list2 = []
    
    for every_thing in list:
        for every_atom in every_thing:
            list2.append(every_atom)
    size_of_list2 = len(list2)
    sqrrt = math.sqrt(size_of_list2)
    #creat a list to match every atom in list2 with  number
    number_match_list = []
    i = 0

    try:
        for every in list2:
            i+=1
            number_match_list.append(i)
        how_far_m_from_end =(size_of_list2 - list2.index('m'))
        how_far_p_from_end =(size_of_list2 - list2.index('p'))
        p_index = list2.index('p')
        m_index = list2.index('m')
        kmr = (list2.index('m')//sqrrt) + 1
        kpr = (list2.index('p')//sqrrt) + 1

        if kmr > kpr:
            print('up by',kmr-kpr,'steps')

        elif kmr < kpr:

            print('down by', kpr - kmr,'steps')

        temp = 0
        tt = list2.index('m')
        kttr = (tt//sqrrt) + 1

        if kpr == kmr:
            if tt > p_index:
                print('left by',m_index - p_index,'steps')
                ini()
                
            else:
                print('right by', p_index - m_index, 'steps')
                ini()
                


        else:
            while temp < sqrrt:
                temp+=1

                if kpr > kmr:
                    tt += sqrrt
                    kttr = (tt//sqrrt) + 1


                    if kttr == kpr:
                        if p_index > tt:
                            print('right by', p_index - tt,'steps')
                            ini()


                        elif p_index < tt:
                            print('left by', tt - p_index, 'steps')
                            ini()
                            

                else:
                    tt -= 4
                    kttr = (tt//sqrrt) + 1


                    if kttr == kpr:
                        if p_index > tt:
                            print('right by', p_index - tt,'steps')
                            ini()
                            
                        elif p_index < tt:
                            print('left by', tt - p_index, 'steps')
                            ini()
                            

    except ValueError:
        print('Value Error guy!')
        ini()

ini()
