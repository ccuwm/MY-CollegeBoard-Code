def choose_and_display(list1, list2):
    # Function to display a list and get a valid index choice from the user
    def get_choice_from_list(item_list, list_name):
        print(f"\nContents of {list_name}:")
        for index, item in enumerate(item_list):
            print(f"{index}: {item}")
        
        # Input validation loop
        while True:
            try:
                choice = int(input(f"\nEnter the index number of the item you want to choose from {list_name} (0-{len(item_list) - 1}): "))
                if 0 <= choice < len(item_list):
                    return item_list[choice]
                else:
                    print(f"Invalid index. Please enter a number between 0 and {len(item_list) - 1}.")
            except ValueError:
                print("Invalid input. Please enter a valid integer.")

    # Get choices from each list
    first_choice = get_choice_from_list(list1, "the hat list")
    second_choice = get_choice_from_list(list2, "the animal list")

    # Display the choices in the specified order
    print("\nYou chose:")
    print(first_choice)
    print(second_choice)


# Sample lists
hatList= (
"""
      /--------.
     |         |
     |      -  |
     | -       |
     |  =      |
   __|_________|__
  (_______________)"""
,
"""
         _____
       _/-. = \ 
     _/______._\ 
    (___________)"""
,
"""
      ______o__
     /- v -    \ 
 ___/___________\ 
(________________)"""
,
"""
               _
             _(/O
           _( \ 
         _(  =\ 
       _(=_   \ 
     _(________\ 
    (___________)"""
,
"""
          ^
         / \ 
        /   \ 
       /=_   \ 
      /-      \ 
     /       _.\ 
    (___________)"""
,
"""
       __  ___
      /  ==   \ 
     /      __ \ 
__  |-.  =      |  __
\ \_/___________\_/ /
 \_________________/"""
,
"""
    ______________
   \=_  PO        |
   _\============/
  (______________)"""
,
"""
      /""--'""\ 
     /-.      =\ 
   _|___________|_
  (_______________)"""
,
"""
      _________
     /         \ 
    |=.         |
    |         _ |
    |___________|"""
,
"""
         |"|
         |_|
        _|_|_
        (OuO)/
        / |
     ____/_\_____
    |=          | 
    |           |
    |           |
    |           |
    |           |
    |      _o   |
    |           |
    |           |
    |           |
    |           |
    |           |
    | -_        |
    |           |
    |           |
    |           |
    |           |
    |         . |
    |           |
    |           |
    |           |
    |           |
    |           |
    | __        |
    |           |
    |           |
    |           |
    |           |
    |           |
    |         - |
    |           |
    |           |
    |           |
    |=.         |
    |___________|
  __|___________|__
 (_________________)"""
)
animalList=(
"""    |  \  /     |
    |  .c .     |
    |  \__/     |
    \           /
     \_________/"""
,
"""    |           |
    |  .c .     |
    |  \__/     |
    \           /
     \_________/"""
,
"""   <|  -    -   |
    |\(|)  (|) / \ 
   [>,-Y----,<  |_\ 
   |  v==v-  /  /
    \________/_/"""
,
"""  __|_.____._   |
 /O          \   \ 
|--v-----    /  |U
 \__________/___/"""
,
"""    |           |
   _|(|)   (|)  |
  /  ..         |
  \--___----)   /
   \___________/
    """
,
"""    |.   .      |
    |/        p)|
    /         / |
   (,,,,,,)     |
    "\IIII     /
     (_(_)____/"""
,
"""    |"-__-""-   |
   /(|)   (|)|  |
  |-==----.   | |
  \ v---v- \   \|
   \_______/___/"""
,
"""  / |           | \ 
 |  | |         |  |
 |  |.|       . |  |
  \ \ \      \ /  /
   \ \_|     //  /
    \_//   _/\__/
      /  _/
      \_ \ 
        \_) *poot* """
,
"""    /______     | 
   /________    |
    |.___.       \ 
    / ''   \      |
    |-----> |    /
     \_____/____/ """
,
"""    |_     __   |
   (  \   /  )  |
    \__\ /__/  /
     \ .     /
      \____/"""
)

choose_and_display(hatList, animalList)
