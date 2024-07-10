# Dotfarmer
My personal dotfile manager, borne out of what I wanted that I wasn't getting (I don't like template files).

# General gist
- `where.json` defines _where_ you want your dots to go, per-platform.

```json
{
    "neovim": { 
        "source": "nvim", <-- relative to your dotfile repo's root. folders supported! :D 
        "windows": "~/AppData/Local/",
        "darwin": "~/.config/",
    }
}
```

- similar to Chezmoi, running `dotfarmer apply` will diff the source state and the target state, and apply changed files

# TODO!
- [ ] Implement basic feature set
    - [ ] Read `where.json`
    - [ ] Diff target state
    - [ ] Apply target state
- [ ] Plan out how to handle per-machine _content_ differences, vs. location differences
    - using templates here is probably fine, just try to minimize complexity as much as humanly possible
