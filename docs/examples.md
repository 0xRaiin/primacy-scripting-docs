## Rendering text with background

<code>
local my_font = render.create_font("Verdana", 24, 400, e_fontflags.antialias | e_fontflags.outline); --create a font
function on_draw()
	local position = point_t.new(1000, 600);
	local text_size = my_font:get_text_size("Hello world!");
	render.draw_rectangle_filled(rect_t.new(position, text_size), color_t.new(0, 0, 0, 150)); --150 for alpha (transparent)
	my_font:draw(position, color_t.new(255, 0, 0), "Hello world!", e_textflags.none);
end
client.set_event_callback("on_draw", on_draw);
</code>