v-if : The block will only be rendered if the directive's expression returns a truthy value.
v-else : You can use the v-else directive to indicate an "else block" for v-if
v-else-if : The v-else-if, as the name suggests, serves as an "else if block" for v-if. It can also be chained multiple times:
v-show : v-show only toggles the display CSS property of the element.

v-if vs. v-show : When v-if and v-for are both used on the same element, v-if will be evaluated first.

summary : v-if has higher toggle costs while v-show has higher initial render costs. So prefer v-show if you need to toggle something very often, and prefer v-if if the condition is unlikely to change at runtime.