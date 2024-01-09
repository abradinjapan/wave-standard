# Wave Standard Library

A set of tools for writing wave code.

# Documentation

## General

- general.character.size()(bytes)
- general.address.size()(bytes)
- general.u8.size()(bytes)
- general.u16.size()(bytes)
- general.u24.size()(bytes)
- general.u32.size()(bytes)
- general.u40.size()(bytes)
- general.u48.size()(bytes)
- general.u56.size()(bytes)
- general.u64.size()(bytes)

## Buffer

- buffer.calculate.size(start end)(length)

## Strings

- string.print.new_line()()
- string.print.space()()
- string.print.tab()()
- string.print(start end)()

## List

- list.offset.buffer_address_start()(value)
- list.offset.buffer_address_end()(value)
- list.offset.buffer_filled_index()(value)
- list.offset.buffer_increase()(value)
- list.size.buffer_address_start()(value)
- list.size.buffer_address_end()(value)
- list.size.buffer_filled_index()(value)
- list.size.buffer_increase()(value)

- list.set.buffer_address_start(list.start value)()
- list.set.buffer_address_end(list.start value)()
- list.set.buffer_filled_index(list.start value)()
- list.set.buffer_increase(list.start value)()

- list.get.buffer_address_start(list.start)(value)
- list.get.buffer_address_end(list.start)(value)
- list.get.buffer_filled_index(list.start)(value)
- list.get.buffer_increase(list.start)(value)

- list.debug.print(list.start list.end)()

- list.create(increase)(list.start list.end error)
- list.destroy(list.start list.end)
- list.expand(list.start)(error)
- list.append(list.start data byte_size)(error)

## Code

- code.write_instruction.setup_pass.measure()(output.current do_write)
- code.write_instruction.setup_pass.build(program_size)(program.start program.end output.current do_write error)
- code.write_instruction(input.current do_write type write_register_value input_0 input_1 input_2 input_3 output_0 output_1 output_2 jump_instruction_ID)(output.current error)

- code.write_instruction.quit(input.current do_write)(output.current error)
- code.write_instruction.write_cell(input.current do_write value destination)(output.current error)
- code.write_instruction.copy_cell(input.current do_write source destination)(output.current error)
- code.write_instruction.print_cell_as_number(input.current do_write source)(output.current error)
- code.write_instruction.print_cell_as_character(input.current do_write source)(output.current error)
- code.write_instruction.get_console_input(input.current do_write buffer.start buffer.end)(output.current error)
- code.write_instruction.create_new_context(input.current do_write cell_count)(output.current error)
- code.write_instruction.restore_old_context(input.current do_write)(output.current error)
- code.write_instruction.pass_input(input.current do_write cell)(output.current error)
- code.write_instruction.get_input(input.current do_write cell)(output.current error)
- code.write_instruction.pass_output(input.current do_write cell)(output.current error)
- code.write_instruction.get_output(input.current do_write cell)(output.current error)
- code.write_instruction.jump_to_abstraction(input.current do_write destination_instruction)(output.current error)
- code.write_instruction.jump_from_abstraction(input.current do_write)(output.current error)
- code.write_instruction.jump(input.current do_write condition jump_instruction_ID)(output.current error)
- code.write_instruction.get_instruction_index(input.current do_write destination)(output.current error)
- code.write_instruction.request_memory(input.current do_write length buffer.start buffer.end error.destination)(output.current error)
- code.write_instruction.return_memory(input.current do_write buffer.start buffer.end)(output.current error)
- code.write_instruction.cell_to_address(input.current do_write source_cell byte_size destination_address error.destination)(output.current error)
- code.write_instruction.address_to_cell(input.current do_write source_address byte_size destination_cell error.destination)(output.current error)
- code.write_instruction.buffer_to_file(input.current do_write buffer.start buffer.end file_path.start file_path.end error.destination)(output.current error)
- code.write_instruction.file_to_buffer(input.current do_write file_path.start file_path.end buffer.start buffer.end error.destination)(output.current error)
- code.write_instruction.integer_add(input.current do_write source_1 source_2 destination)(output.current error)
- code.write_instruction.integer_subtract(input.current do_write source_1 source_2 destination)(output.current error)
- code.write_instruction.integer_multiply(input.current do_write source_1 source_2 destination)(output.current error)
- code.write_instruction.integer_divide(input.current do_write source_1 source_2 destination error.destination)(output.current error)
- code.write_instruction.integer_modulous(input.current do_write source_1 source_2 destination error.destination)(output.current error)
- code.write_instruction.integer_within_range(input.current do_write low_bound value high_bound destination)(output.current error)
- code.write_instruction.boolean_not(input.current do_write source destination)(output.current error)
- code.write_instruction.get_context_input(input.current do_write destination.start destination.end)(output.current error)
- code.write_instruction.pass_context_output(input.current do_write source.start source.end)(output.current error)
- code.write_instruction.run(input.current do_write program.start program.end input.start input.end result.start result.end runner_error.destination)(output.current error)
