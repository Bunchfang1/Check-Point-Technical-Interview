class Node:
    def __init__(self, name, is_dir=False):
        self.name = name
        self.is_dir = is_dir
        self.children = []

class FileSystem:
    def __init__(self):
        self.root = Node("/", is_dir=True)
        self.current_node = self.root

    def mkdir(self, name):
        new_dir = Node(name, is_dir=True)
        self.current_node.children.append(new_dir)

    def cd(self, name):
        if name == "..":
            if self.current_node != self.root:
                self.current_node = self._get_parent(self.current_node)
        else:
            child = self._get_child_by_name(self.current_node, name)
            if child and child.is_dir:
                self.current_node = child

    def touch(self, name):
        new_file = Node(name)
        self.current_node.children.append(new_file)

    def ls(self):
        contents = [node.name for node in self.current_node.children]
        return contents

    def _get_child_by_name(self, node, name):
        for child in node.children:
            if child.name == name:
                return child
        return None

    def _get_parent(self, node):
        if node == self.root:
            return None

        for child in self.root.children:
            if node in child.children:
                return child
            else:
                parent = self._get_parent(node)
                if parent:
                    return parent
        return None

def main():
    fs = FileSystem()
    while True:
        command = input("Enter command (mkdir <name>, cd <name>, touch <name>, ls, exit): ").split()
        if command[0] == "mkdir":
            fs.mkdir(command[1])
        elif command[0] == "cd":
            fs.cd(command[1])
        elif command[0] == "touch":
            fs.touch(command[1])
        elif command[0] == "ls":
            print("Contents of current directory:", fs.ls())
        elif command[0] == "exit":
            print("Exiting...")
            break
        else:
            print("Invalid command.")

if __name__ == "__main__":
    main()
