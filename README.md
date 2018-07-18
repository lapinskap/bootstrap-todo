# bootstrap-todo
> Ruby on Rails application with linked Bootstrap. 

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info
General purpose was to add Bootstrap to Ruby on Rails project. It was not as easy as it seems! bootstrap-sass gem was problematic.

Simple "todo" application, without any special features, can be used to test new gems.

I need to implement my own styles alongside bootstrap to make it look like real application


## Screenshots
![Example screenshot](./img/screenshot.png)

## Technologies
* Ruby on Rails 5
* Bootstrap 5

## Setup
```
git clone https://github.com/lapinskap/bootstrap-todo/
cd bootstrap-todo
bundle install
rails s
```

## Code Examples

POST action in ./app/controllers/todos_controller.rb
```ruby
  # POST /todos
  # POST /todos.json
  def create
    @todo = Todo.new(todo_params)

    respond_to do |format|
      if @todo.save
        format.html { redirect_to @todo, notice: 'Todo was successfully created.' }
        format.json { render :show, status: :created, location: @todo }
      else
        format.html { render :new }
        format.json { render json: @todo.errors, status: :unprocessable_entity }
      end
    end
  end
```

## Features
List of features ready and TODOs for future development
* Awesome bootstrap link 
* Awesome jquery link

To-do list:
* try to use bootstrap-sass gem again!

## Status
Project is: _in progress_

## Inspiration

My very trivial problems with the bootstrap implementation were the inspiration...

## Contact
Created by [@lapinskap](https://www.facebook.com/paulina.lapinska99) - feel free to contact me!
