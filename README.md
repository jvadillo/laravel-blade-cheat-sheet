# laravel-blade-cheat-sheet
Blade template engine cheat sheet


```php
// Definir un layout
@yield('name')
@section('name')
@endsection/@show

// Extender Layout
@extends('template')

@section('name') ... content ... @endsection
@section('name', 'value')
@section('name', $value)

// Mostrar contenido de cariables
{{$name}} // escaped
{{$name or 'Default'}} // if not set
{!! $name !!} // unescaped
@{{ name }} // ignore braces - output as is
@verbatim // ignore all braces in this block @endverbatim

// If 
@if, @elseif, @else and @endif
@unless, @endunless

// Iterar
@for...@endfor
@foreach...@endforeach
@forelse...@empty...@endforelse
@while...@endwhile
@continue, @continue($user->type==1)
@break, $break($user->type==1)
$loop - index, iteration, remaining, count, first, last, depth, parent

// Comentarios
{{-- This comment will not be present in the rendered HTML --}}

// PHP
@php...@endphp

// Incluir vistas
@include('template')
@include('template', ['some' => 'data'])
@includeIf('not_exist', ['some' => 'data']) // won't an error
@each('jobtemplate', $jobs, 'job', 'emptyresult')
```
