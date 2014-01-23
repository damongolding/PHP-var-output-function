# This or that function for SASS

## What is it?

This function switchs which item in a SASS list variable is outputted with a global $var.

This could be used for many things but I have used it to either output a SASS var or echo a PHP var

## Example

### SASS

	$sass: true; <- Determins which output to use

	$mainColour: #fff "$mainColour"; <- make a list sass var (var with two items in it, the seconed being the name of the var)

	.Foo{
		background: phpOut($mainColour);
	}

### CSS output 1 ($SASS: true)
	.Foo{
		background-color: #ffffff;
	}

### CSS output 2 ($SASS:false)
	.Foo{
		background-color: <?php echo $mainColour; ?>;
	}


