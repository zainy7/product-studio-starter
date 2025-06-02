"use client";

import React from 'react';
import TaskList from '@/components/task/TaskList';
import { tasks } from '@/lib/data';

const Page = () => {
    return (
        <div>
            <TaskList tasks={tasks} />
        </div>
    );
};

export default Page;
