# Asynchronous spelling checker for Neovim
# Requirements: aspell

# Config example
augroup SpellingUpdateGroup
    autocmd!
    autocmd InsertLeave * SpellingUpdate
    autocmd BufWrite * SpellingUpdate
    autocmd BufEnter * SpellingUpdate
    autocmd WinEnter * SpellingUpdate
augroup END
autocmd ColorScheme * highlight SpellBad cterm=underline gui=underline ctermfg=243 guifg=#727272

nnoremap <leader>st :SpellingToggle<cr>
nnoremap <leader>sa :SpellingAddWord<cr>
