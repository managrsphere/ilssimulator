<template>
  <div>
    <Card>
      <CardHeader>
        <CardTitle>Einsatzmittel</CardTitle>
        <CardDescription>Einsatzmittel für den aktuellen Einsatz</CardDescription>
      </CardHeader>
      <CardContent>
        <Input class="w-1/2" placeholder="Einsatzmittel hinzufügen"></Input>
        <div class="pt-4">
          <Table>
            <TableCaption>Vorschlag</TableCaption>
            <TableHeader>
              <TableRow>
                <TableHead class="w-1/3">Funkrufname</TableHead>
                <TableHead class="w-[100px]">Status</TableHead>
                <TableHead class="w-[100px]">Entfernung</TableHead>
                <TableHead class="w-[100px]">Entfernung Luftlinie</TableHead>
              </TableRow>
            </TableHeader>
            <TableBody>
              <TableRow v-for="em in vorschlag">
                <TableCell class="font-medium">
                  {{ em.funkrufname }}
                </TableCell>
                <TableCell>{{ em.status }}</TableCell>
                <TableCell>{{ em.distance }}</TableCell>
                <TableCell>{{ em.luftlinie }}</TableCell>
              </TableRow>
            </TableBody>
          </Table>
        </div>
        <div class="flex flex-row pt-4 justify-end">
          <Button variant="destructive" @click="alarmieren">Alarmieren</Button>
        </div>
        <div class="pt-4">
          <Table>
            <TableCaption>Alle Einsatzmittel im aktuellen Einsatz</TableCaption>
            <TableHeader>
              <TableRow>
                <TableHead class="w-1/3">Funkrufname</TableHead>
                <TableHead class="w-[100px]">Status</TableHead>
                <TableHead class="w-[100px]">C</TableHead>
                <TableHead class="w-[100px]">S3</TableHead>
                <TableHead class="w-[100px]">S4</TableHead>
                <TableHead class="w-[100px]">S7</TableHead>
                <TableHead class="w-[100px]">S8</TableHead>
                <TableHead class="w-[100px]">S1</TableHead>
                <TableHead class="w-[100px]">S2</TableHead>
              </TableRow>
            </TableHeader>
            <TableBody>
              <TableRow v-for="em in alarmiert">
                <TableCell class="font-medium">
                  {{ em.funkrufname }}
                </TableCell>
                <TableCell>{{ em.status }}</TableCell>
                <TableCell>{{ em.c }}</TableCell>
                <TableCell>{{ em.s3 }}</TableCell>
                <TableCell>{{ em.s4 }}</TableCell>
                <TableCell>{{ em.s7 }}</TableCell>
                <TableCell>{{ em.s8 }}</TableCell>
                <TableCell>{{ em.s1 }}</TableCell>
                <TableCell>{{ em.s2 }}</TableCell>
              </TableRow>
            </TableBody>
          </Table>
        </div>
      </CardContent>
      <CardFooter>
      </CardFooter>
    </Card>
  </div>
</template>

<script lang="ts" setup>
import {
  Card,
  CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'

import {
  Table,
  TableBody,
  TableCaption,
  TableCell,
  TableHead,
  TableHeader,
  TableRow,
} from '@/components/ui/table'

import { Input } from '@/components/ui/input';
import { Button } from '@/components/ui/button';

interface IEinsatzmittel {
  funkrufname: string,
  status: number,
  distance: string,
  luftlinie: string,
  c?: string,
  s3?: string,
  s4?: string,
  s7?: string,
  s8?: string,
  s1?: string,
  s2?: string
}

const vorschlag = ref<Array<IEinsatzmittel>>([
  {
    funkrufname: "Rotkreuz Regensburg 21/12/2",
    status: 2,
    distance: "1,4km",
    luftlinie: "900m",
  }
]);
const alarmiert = ref<Array<IEinsatzmittel>>([
  {
    funkrufname: "Rotkreuz Regensburg 8/1",
    status: 4,
    distance: "1,4km",
    luftlinie: "900m",
    c: "12:27",
    s3: "12:30",
    s4: "12:38",
    s7: "13:04",
    s8: "13:20",
    s1: "13:44",
    s2: "14:02"
  }
]);

function alarmieren() {
  vorschlag.value.forEach((em: IEinsatzmittel) => {
    em.c = new Date().toString();
  });
  alarmiert.value = alarmiert.value.concat(vorschlag.value);
  vorschlag.value = [];
}
</script>

<style></style>