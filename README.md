# Wave Standard Library

A set of tools for writing wave code.

# Documentation

## General

- general.character.size()(bytes)

- general.address.size()(bytes)

- general.u64.size()(bytes)

## Buffer

- buffer.copy.same_size(old.start old.end new.start new.end)(error)

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
