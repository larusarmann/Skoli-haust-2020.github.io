# Skoli-haust-2020
 allt skóla drasl

 * [Github](https://github.com/larusarmann/larusarmann.github.io)

Vefhönnun 2020
Lárus Ármann Kjartansson

-----------------------------------------------------------------------

VERKEFNI 1

  * [VERKEFNI 1 auglýsing](Vefhönnun/Verkefni_1-auglýsing/anim.html)


{{- $.Scratch.Set "theHref"    "#"                                }}
{{- $.Scratch.Set "theIcon"    ""                                 }}
{{- $.Scratch.Set "theClasses" "w3-button w3-ripple w3-theme-l3 " }}
{{- if .IsNamedParams }}
  {{- $.Scratch.Set "theHref"    (.Get "href"    | default ($.Scratch.Get "theHref")    )}}
  {{- $.Scratch.Set "theIcon"    (.Get "icon"    | default ($.Scratch.Get "theIcon")    )}}
  {{- $.Scratch.Set "theClasses" (.Get "classes" | default ($.Scratch.Get "theClasses") ) }}
{{- else}}
  {{- $myPos := 0}} {{ if gt (len .Params) $myPos }} {{$.Scratch.Set "theHref"    (.Get $myPos) }} {{end}}
  {{- $myPos := 1}} {{ if gt (len .Params) $myPos }} {{$.Scratch.Set "theIcon"    (.Get $myPos) }} {{end}}
  {{- $myPos := 2}} {{ if gt (len .Params) $myPos }} {{$.Scratch.Set "theClasses" (.Get $myPos) }} {{end}}
{{- end}}
<a class="{{$.Scratch.Get `theClasses`}}" href="{{$.Scratch.Get `theHref` | relURL }}">{{if $.Scratch.Get `theIcon`}}<i class="{{$.https://larusarmann.github.io/Skoli-haust-2020/ `theIcon`}} fa-1x"></i>{{end}}&nbsp;{{ .Inner }}</a>
