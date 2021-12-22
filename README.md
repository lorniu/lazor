# lazor

There are `cl-who` and `djula` and others in common lisp for render a html page.

They are good, but I prefer something like Razor in asp.net.

A template engine, which syntax like below:
```lisp
@(setq layout "x")

<section>
  <header>
    @(if items
         <span>Total: @(length items) items</span>
         (progn
            <span>Nothing found.</span>
            @(html 'a "click me")
      ))
  </header>
  <div class="xxx">
    @(loop for i in items
           do <a href="@(car i)">@(cdr i)</a>)
  </div>
</section>

@(render 'style
    .xxx {
       color: red;
    }
)
```

Now it's an idea. Maybe someday implement It.


