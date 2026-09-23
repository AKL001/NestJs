# NestJs 

# NOTES 
    - Client 
    - Controller : Handles HTTP requests & response
    - Sevices : Hanldes logic

# Controller Decorator (@Contorller)
    - Routing example :
    ```
import { Controller, Get } from '@nestjs/common';

@Controller('cats')
export class CatsController {
  @Get()
  findAll(): string {
    return 'This action returns all cats';
  }
}
``` 
 - to access the request details we could use the @Req() object 
 ```findAll(@Req() request: Request): string {
    return 'This action returns all cats';
  }```

```
@Post()
create(@Body({ schema: createCatSchema }) createCatDto: CreateCatDto) {
  return this.catsService.create(createCatDto);
}

@Get(':id')
findOne(@Param('id', { schema: z.coerce.number().int().positive() }) id: number) {
  return this.catsService.findOne(id);
}
```
- DTO -> we make the DTO for shape form 

# making our costom decorators 


# PROVIDER 
    ## SERVICES 
        - 