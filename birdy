#!/usr/bin/env python3

import sys

def help():
    print("Help!")

def install(package):
    print(f"Installed {package}")

def search(query):
    print(f"Searching for {query}")

def publish(packagename):
    print(f"Published {packagename}")

def main():
    if len(sys.argv) == 1:
        help()
        return

    try:
        arg1 = sys.argv[1]
    except IndexError:
        arg1 = None
    
    try:
        arg2 = sys.argv[2]
    except IndexError:
        arg2 = None

    if arg1 == 'help':
        help()
    
    elif arg1 == 'publish':
        packagename = arg2
        if packagename == None:
            help()
        else:
            publish(packagename)
    else:
        package = arg1
        if arg2 == '-y':
            install(package)
        elif arg2 == '-n':
            search(package)
        else:
            response = input(f"Do you want to install {package}? (y/n): ")
            if response.lower() == 'y':
                install(package)
            if response.lower() == 'n':
                search(query)
if __name__ == "__main__":
    main()
