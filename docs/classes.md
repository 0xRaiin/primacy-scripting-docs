## client

> STATIC <code>set_event_callback(event: string, callback: function(...))</code>


## core
> <p><code>m_globals: interface</code></p>
> <p><code>m_engine: interface</code></p>
> <p><code>m_panorama: interface</code></p>


## core.m_global_vars

> <code>get_real_time(): float</code>

> <code>get_frame_count(): float</code>

> <code>get_frame_time(): float</code>

> <code>get_server_time(): float</code>

> <code>get_max_clients(): number</code>

> <code>get_tick_count(): number</code>

> <code>get_interval_per_tick(): float</code>

> <code>get_tick_rate(): number</code>

> <code>get_frame_rate(): number</code>


## core.m_engine

> <code>connected_in_game(): boolean</code>

> <code>is_taking_screenshot(): boolean</code>

> <code>set_view_angles(angles: vec3_t)</code>

> <code>get_view_angles(): vec3_t</code>

> <code>is_voice_recording(): boolean</code>

> <code>execute_cmd(command: string)</code>


## core.m_panorama

> <code>run_script(script: string)</code>


## memory

> <code>scan_pattern(module: string, pattern: string): number</code>- needs to be an IDA-style pattern

> <code>get_v_func(address: number, index: number): number</code>


## color_t

> <p><code>r: number</code></p>
> <p><code>g: number</code></p>
> <p><code>b: number</code></p>
> <p><code>a: number</code></p>

> <code>constructor()</code>- defaults to rgba(255, 255, 255, 255)

> <code>constructor(r: number, g: number, b: number, [a: number])</code>

> <code>interpolate(other_color: color_t, progress: float{ 0-1 })</code>- linear rgba transition from one color to another

> <code>interpolate_hsv(other_color: color_t, progress: float{ 0-1 })</code>- linear hsv transition from one color to another


## c_handle

> <code>get_index(): number</code>

> <code>is_valid(): boolean</code>- return whether index is valid or not


## c_entity

> STATIC <code>get_entity_from_id(): c_base_entity</code>

> STATIC <code>get_entity_from_id(handle: c_base_handle): c_base_entity</code>

> <code>is_player(): boolean</code>

> <code>is_weapon(): boolean</code>

> <code>is_dormant(): boolean</code>

> <code>get_index(): number</code>

> <code>get_abs_origin(): vec3_t</code>

> <code>get_abs_angles(): vec3_t</code>

> <code>get_prop_bool(field: string): boolean</code>

> <code>get_prop_int(field: string): number</code>

> <code>get_prop_float(field: string): float</code>

> <code>get_prop_vec3_t(field: string): vec3_t</code>

> <code>get_prop_handle(field: string): handle</code>

> <code>set_prop_bool(field: string, value: boolean)</code>

> <code>set_prop_int(field: string, value: number)</code>

> <code>set_prop_float(field: string, value: float)</code>

> <code>set_prop_vec3_t(field: string, value: vec3_t)</code>

> <code>set_prop_handle(field: string, value: handle)</code>


## c_player

- <a href="#/classes?id=c_base_entity">c_base_entity</a>

> STATIC <code>get_player_from_id(): c_base_player</code>

> STATIC <code>get_player_from_id(handle: c_base_handle): c_base_player</code>

> STATIC <code>get_local_player(): c_base_player</code>

> <code>is_valid(): boolean</code>- checks if player is alive and not dormant

> <code>is_enemy(): boolean</code>


## c_weapon

- <a href="#/classes?id=c_base_entity">c_base_entity</a>

> STATIC <code>get_weapon_from_id(): object</code>

> STATIC <code>get_weapon_from_handle(handle: c_base_handle): object</code>

> <code>get_weapon_data(): weapon_data_t</code>


## weapon_data_t

> <p><code>m_weapon_name; string [read-only]</code></p>
> <p><code>m_weapon_type: number [read-only]</code></p>
> <p><code>m_world_model; string [read-only]</code></p>
> <p><code>m_view_model; string [read-only]</code></p>
> <p><code>m_dropped_model; string [read-only]</code></p>
> <p><code>m_max_ammo: number [read-only]</code></p>
> <p><code>m_max_reserve_ammo: number [read-only]</code></p>
> <p><code>m_range: float [read-only]</code></p>


## user_cmd_t

> <p><code>m_command_number; number [read-only]</code></p>
> <p><code>m_tick_count: number [read-only]</code></p>
> <p><code>m_viewangles: vec3_t</code></p>
> <p><code>m_aimdirection: vec3_t</code></p>
> <p><code>m_move: vec3_t</code></p>
> <p><code>m_buttons: number</code></p>
> <p><code>m_impulse: bool</code></p>
> <p><code>m_weaponselect: number [read-only]</code></p>
> <p><code>m_weaponsubtype: number [read-only]</code></p>
> <p><code>m_random_seed: number [read-only]</code></p>
> <p><code>m_mousedx: short</code></p>
> <p><code>m_mousedy: short</code></p>
> <p><code>m_hasbeenpredicted: boolean</code></p>


## render

> STATIC <code>get_screen_resolution(): point_t</code>

> STATIC <code>set_rotation(degrees: float)</code>

> STATIC <code>pop_rotation()</code>

> STATIC <code>set_clip(rect: rect_t)</code>

> STATIC <code>get_clip(): rect_t</code>

> STATIC <code>pop_clip()</code>

> STATIC <code>path_to(point: point_t)</code>

> STATIC <code>path_stroke(color: color_t, closed: boolean, thickness: number)</code>

> STATIC <code>path_fill(color: color_t)</code>

> STATIC <code>path_end()</code>

> STATIC <code>create_font(type_name: string, size: number, weight: number, flags: e_fontflags): font_t</code>

> STATIC <code>draw_rectangle(rect: rect_t, color: color_t, [rounding: number])</code>

> STATIC <code>draw_rectangle_filled(rect: rect_t, color: color_t, [rounding: number])</code>

> STATIC <code>draw_rectangle_filled(rect: rect_t, color: color_t, color_gradient: color_t, horizontal: boolean, [rounding: number])</code>- gradient

> STATIC <code>draw_circle(position: point_t, radius: number, filled: boolean)</code>

> STATIC <code>draw_image(rect: rect_t, texture: c_texture, [rounding: number])</code>

> STATIC <code>get_texture_file(path: string, size: point_t): c_texture</code>

> STATIC <code>get_texture_file_svg(path: string): c_texture</code>

> STATIC <code>get_texture_memory(key: string, data:string, size: point_t): c_texture</code>

> STATIC <code>get_texture_memory_svg(key: string, data: string): c_texture</code>

> STATIC <code>get_texture_by_key(key: string): c_texture</code>

> STATIC <code>delete_cached_texture(key: string)</code>

## c_texture

> <code>set_size(size: point_t)</code>

> <code>scale_size(scale: float)</code>

> <code>get_size(): point_t</code>


## font_t

> <code>draw(position: point_t, [bounds_x: number], color: color_t, text: string, flags: e_textflags)</code> --bounds_x is optional. it decides when text will draw in a new line.

> <code>get_text_size(text: string, [bounds_x]): point_t</code> --bounds_x is optional. it decides when text will draw in a new line.


## c_vpk

> STATIC <code>get_texture_png(archive: string, texture_name: string, path: string, size: point_t): c_texture</code>

> STATIC <code>get_texture_svg(archive: string, texture_name: string, path: string): c_texture</code>


## math

> STATIC <code>world_to_screen(world: vec3_t): point_t</code>

> STATIC <code>calc_angle(src: vec3_t, dst: vec3_t): vec3_t</code>


## point_t

> <p><code>x: number</code></p>
> <p><code>y: number</code></p>


## points_t

> <p><code>m_left: number</code></p>
> <p><code>m_top: number</code></p>
> <p><code>m_right: number</code></p>
> <p><code>m_bottom: number</code></p>


## rect_t

> <p><code>m_position: point_t</code></p>
> <p><code>m_size: point_t</code></p>
> <p><code>m_points: points_t</code></p> -POINTS_t NOT POINT_T

> <code>update_points()</code>

## vec3_t

> <p><code>x: float</code></p>
> <p><code>y: float</code></p>
> <p><code>z: float</code></p>

> <code>length(): float</code>


## gui

> STATIC <code>create_tab(title: string): <a href="#/classes?id=c_gui_parent">c_gui_parent</a></code>

> STATIC <code>get_element_traverse(title: string): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

## c_gui_element

> <code>set_title(title: string)</code>

> <code>get_title(): string</code>

> <code>set_position(position: point_t)</code>

> <code>get_position(): point_t</code>

> <code>set_size(position: point_t)</code>

> <code>get_size(): point_t</code>

> <code>get_geometry_area(): <a href="#/classes?id=rect_t">rect_t</a></code>

> <code>get_geometry_area_relative(): <a href="#/classes?id=rect_t">rect_t</a></code>

> <code>set_value(title: any)</code>

> <code>get_value_number(): number</code>

> <code>get_value_float(): float</code>

> <code>get_value_boolean(): boolean</code>

> <code>get_value_color(): color_t</code>

> <code>get_value_string(): string</code>


## c_gui_parent

- <a href="#/classes?id=c_gui_element">c_gui_element</a>

- The titles are IMPORTANT for configs. Set a title for every element you create

> <code>groupbox(title: string, position: point_t, [size: point_t]): <a href="#/classes?id=c_gui_parent">c_gui_parent</a></code>

> <code>checkbox(title: string, [margin_top: number]): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

> <code>switchbox(title: string, [margin_top: number]): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

> <code>slider_int(title: string, min: number, max: number, [margin_top: number]): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

> <code>slider_float(title: string, min: float, max: float, [margin_top: number]): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

> <code>dropdown(title: string, options: { ... } string, [margin_top: number]): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

> <code>list_box(title: string, options: { ... } string, height: number): <a href="#/classes?id=c_gui_selectable">c_gui_selectable</a></code>

> <code>colorpicker(title: string, show_title: boolean, same_line: boolean margin_top: number, margin_right: number): <a href="#/classes?id=c_gui_element">c_variable_controller</a></code>

> <code>text_box(title: string, margin_top: number): <a href="#/classes?id=c_gui_element">c_gui_element</a></code>

## c_groupbox

- <a href="#/classes?id=c_gui_parent">c_gui_parent</a>


## c_gui_selectable

- <a href="#/classes?id=c_gui_element">c_gui_element</a>

> <code>set_input_callback(callback: function(index: number))</code>

> <code>set_is_selected_callback(callback: function(index: number): boolean)</code>

> <code>set_is_enabled(callback: function(index: number): boolean)</code>


## cheat

> <code>m_user_data: interface</code>


## cheat.m_user_data

> <code>get_uid(): number</code>

> <code>get_username(): string</code>

> <code>get_subscription(): string</code>


## c_http_request

> <code>constructor(host: string, args: string, method: e_request_method)</code>

> <code>constructor(url: string, method: e_request_method)</code>

> <code>set_body(body: string)</code>

> <code>add_header(header: string)</code>

> <code>send(force_https: boolean): <a href="#/classes?id=http_response_t">http_response_t</a></code>


## http_response_t

> <p><code>m_status_code: number [read-only]</code></p>
> <p><code>m_text: string [read-only]</code></p>
